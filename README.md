[![Docker Build](https://github.com/ai-dock/python/actions/workflows/docker-build.yml/badge.svg)](https://github.com/ai-dock/python/actions/workflows/docker-build.yml)

# AI-Dock + Python

Run python in a cloud-first AI-Dock container. Nothing is added to the installed python environment(s) - You'll have python & pip.

This image provides a great starting point for python development when used standalone but its also a solid foundation for extending upon.

## Documentation

All AI-Dock containers share a common base which is designed to make running on cloud services such as [vast.ai](https://link.ai-dock.org/vast.ai) and [runpod.io](https://link.ai-dock.org/template) as straightforward and user friendly as possible.

Common features and options are documented in the [base wiki](https://github.com/ai-dock/base-image/wiki) but any additional features common to this image will be detailed below.


## Version Tags

The `:latest` tag points to `:latest-cuda`

Tags follow these patterns:

##### _CUDA_
- `:[python-version]-cuda-[x.x.x]-[base|runtime|devel]-[ubuntu-version]`

- `:latest-cuda` &rarr; `:3.12-cuda-12.3.1-runtime-22.04`

##### _ROCm_
- `:[python-version]-rocm-[x.x.x]-[core|runtime]-[ubuntu-version]`

- `:latest-rocm` &rarr; `:3.12-rocm-6.0.2-runtime-22.04`

ROCm builds are experimental. Please give feedback.

##### _CPU_
- `:[python-version]-cpu-[ubuntu-version]`

- `:latest-cpu` &rarr; `:3.12-cpu-22.04`

Browse [here](https://github.com/ai-dock/python/pkgs/container/python) for an image suitable for your target environment.

Supported Python versions: `3.12`, `3.11`, `3.10`

Supported Platforms: `NVIDIA CUDA`, `AMD ROCm`, `CPU`


## Aditional Micromamba Environments

These environments are included alongside the [defaults](https://github.com/ai-dock/base-image/wiki/1.0-Included-Software#installed-micromamba-environments).

| Environment    | Packages |
| -------------- | ----------------------------------------- |
| `python_[ver]` | `python` |


## Pre-Configured Templates

**Vast.​ai**

[python:latest](https://link.ai-dock.org/template-vast-python)

---

**Runpod.​io**

[python:latest](https://link.ai-dock.org/template-runpod-python)

---

>[!NOTE]  
>These templates are configured to use the `latest` tag but you are free to change to any of the available Python CUDA tags listed [here](https://github.com/ai-dock/python/pkgs/container/python)

---

_The author ([@robballantyne](https://github.com/robballantyne)) may be compensated if you sign up to services linked in this document. Testing multiple variants of GPU images in many different environments is both costly and time-consuming; This along with [sponsorships](https://github.com/sponsors/ai-dock) helps to offset costs and further the development of the project_

