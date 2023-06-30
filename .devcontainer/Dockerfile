FROM ubuntu:jammy
MAINTAINER Open Source Integrators <support@opensourceintegrators.com>

SHELL ["/bin/bash", "-xo", "pipefail", "-c"]

# Generate locale C.UTF-8
ENV LANG C.UTF-8
ENV TZ=Europe/Berlin
RUN ln -snf /usr/share/zoneinfo/$TZ /etc/localtime && echo $TZ > /etc/timezone

RUN apt update \
  && apt upgrade -y \
  && apt install -y --no-install-recommends \
    ca-certificates \
    curl \
    htop \
    iotop \
    rsync \
    tar \
    vim \
    unzip \
  && apt clean all \
  && apt autoremove

