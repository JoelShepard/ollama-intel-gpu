# This is a fork

# ollama-intel-gpu

This repo illlustrates the use of Ollama with support for Intel ARC GPU based via ipex-llm.

# Prerequisites
* Recent Linux Distro (for Intel ARC GPU kernel driver support. Tested with Fedora 41).
* Installed Docker and Docker-compose tools (for Linux)
* Intel ARC series GPU. Tested with iGPU Iris Xe Intel i7-1260P.

*Note:* This branch uses the upstream ipex container published by Intel.  See the alternate branch [alternate_base_image](https://github.com/mattcurf/ollama-intel-gpu/tree/alternate_base_image) for an equivalent Dockerfile which builds everything from the published packages directly.

# Usage

The following will build the Ollama with Intel ARC GPU support, and compose those with the public docker image based on OpenWEB UI from https://github.com/open-webui/open-webui

Linux:
```bash
$ git clone https://github.com/mattcurf/ollama-intel-gpu
$ cd ollama-intel-gpu
$ docker compose up 
```

*Note:* you will see the following message.  This is expected and harmless, as the docker image 'ollama-intel-gpu' is built locally.
```
ollama-intel-gpu Warning pull access denied for ollama-intel-gpu, repository does not exist or may require 'docker login': denied: requested access to the resource is denied
```

# References
* https://dgpu-docs.intel.com/driver/client/overview.html
* https://ipex-llm.readthedocs.io/en/latest/doc/LLM/Quickstart/ollama_quickstart.html
