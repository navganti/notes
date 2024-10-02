---
aliases: [C++ Virtual Environments]
tags: [cpp, programming]
---
# C++ Virtual Environments

Through tools such as [Pyenv](https://github.com/pyenv/pyenv-virtualenv) or [Conda](https://docs.conda.io/en/latest/), programmers can create an isolated environment for individual Python projects, which each has its own dependencies.

For C++, this seems to only be possible via [Docker](https://www.docker.com/), which creates a container that is isolated from the host environment. I think of Docker containers akin to a virtual machine, although it's just an application process. For my specific use cases, this is pretty similar, although Docker is significantly more powerful.

>[!question]
Is it possible to create a Python-esque virtual environment for C++ programs, without using Docker?

I think I will have to look into more C++ package managers, such as [Conan](https://conan.io/) or [Vcpkg](https://github.com/microsoft/vcpkg), as well as build systems like [CMake](https://cmake.org/) or [Meson](https://mesonbuild.com/).

## Related

## References
