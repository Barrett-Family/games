# [Choice] Python version (use -bookworm or -bullseye variants on local arm64/Apple Silicon): 3, 3.12, 3.11, 3.10, 3.9, 3.8, 3-bookworm, 3.12-bookworm, 3.11-bookworm, 3.10-bookworm, 3.9-bookworm, 3.8-bookworm, 3-bullseye, 3.12-bullseye, 3.11-bullseye, 3.10-bullseye, 3.9-bullseye, 3.8-bullseye, 3-buster, 3.12-buster, 3.11-buster, 3.10-buster, 3.9-buster, 3.8-buster
ARG VARIANT=3-bookworm
FROM python:${VARIANT}

RUN apt-get update && export DEBIAN_FRONTEND=noninteractive

RUN python3 -m pip install --upgrade \
    setuptools==69.0.3 \
    gitpython==3.1.41 \
    pygame==2.5.2 \
    pyxel==2.0.10 \
    arcade==2.6.17

# [Optional] Uncomment this section to install additional OS packages.
RUN apt-get update && export DEBIAN_FRONTEND=noninteractive \
    && apt-get -y install --no-install-recommends libjpeg-dev zlib1g-dev libsdl2-dev firefox-esr alsaplayer-common alsa-utils libasound2-dev libglib2.0-dev

# [Optional] Uncomment this line to install global node packages.
# RUN su vscode -c "source /usr/local/share/nvm/nvm.sh && npm install -g <your-package-here>" 2>&1
