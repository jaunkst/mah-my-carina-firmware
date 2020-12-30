# See here for image contents: https://github.com/microsoft/vscode-dev-containers/tree/v0.154.0/containers/ubuntu/.devcontainer/base.Dockerfile

# [Choice] Ubuntu version: bionic, focal
ARG VARIANT="focal"
FROM mcr.microsoft.com/vscode/devcontainers/base:0-${VARIANT}

# [Optional] Uncomment this section to install additional OS packages.
RUN apt-get update && export DEBIAN_FRONTEND=noninteractive \
    && apt-get -y install --no-install-recommends build-essential gcc-arm-none-eabi libnewlib-arm-none-eabi libusb-1.0-0-dev wget git python3-pip

RUN wget https://github.com/Massdrop/mdloader/releases/download/1.0.5/applet-mdflash.bin
RUN wget https://github.com/Massdrop/mdloader/releases/download/1.0.5/mdloader_linux
RUN chmod +x ./mdloader_linux

RUN ln -s /mdloader_linux /bin/mdloader

RUN pip3 install appdirs argcomplete colorama