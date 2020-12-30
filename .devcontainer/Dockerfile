# See here for image contents: https://github.com/microsoft/vscode-dev-containers/tree/v0.154.0/containers/typescript-node/.devcontainer/base.Dockerfile

# [Choice] Node.js version: 14, 12, 10
ARG VARIANT="14-buster"
FROM mcr.microsoft.com/vscode/devcontainers/typescript-node:0-${VARIANT}

# [Optional] Uncomment this section to install additional OS packages.
# RUN apt-get update && export DEBIAN_FRONTEND=noninteractive \
#     && apt-get -y install --no-install-recommends <your-package-list-here>

# [Optional] Uncomment if you want to install an additional version of node using nvm
# ARG EXTRA_NODE_VERSION=10
# RUN su node -c "source /usr/local/share/nvm/nvm.sh && nvm install ${EXTRA_NODE_VERSION}"

# [Optional] Uncomment if you want to install more global node packages
# RUN sudo -u node npm install -g <your-package-list -here>


# [Optional] Uncomment this section to install additional OS packages.
RUN apt-get update && export DEBIAN_FRONTEND=noninteractive \
    && apt-get -y install --no-install-recommends build-essential gcc-arm-none-eabi libnewlib-arm-none-eabi libusb-1.0-0-dev wget git

# RUN npm install yarn -g

RUN wget https://github.com/Massdrop/mdloader/releases/download/1.0.5/applet-mdflash.bin
RUN wget https://github.com/Massdrop/mdloader/releases/download/1.0.5/mdloader_linux
RUN chmod +x ./mdloader_linux

# RUN ln -s /mdloader_linux /bin/mdloader
# RUN ln -s /applet-mdflash.bin /bin/applet-mdflash.bin

