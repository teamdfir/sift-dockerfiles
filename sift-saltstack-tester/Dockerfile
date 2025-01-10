ARG OSVERSION=24.04

FROM ubuntu:$OSVERSION

ARG OSVERSION=24.04
ARG SALTVERSION=3006
ARG OSCODE=noble

ENV DEBIAN_FRONTEND=noninteractive

RUN \
  apt-get update && \
  apt-get install -y wget gnupg git && \
  wget -O - "https://packages.broadcom.com/artifactory/api/security/keypair/SaltProjectKey/public" | tee /etc/apt/keyrings/salt-archive-keyring.pgp && \
  wget -O - "https://github.com/saltstack/salt-install-guide/releases/latest/download/salt.sources" | tee /etc/apt/sources.list.d/salt.sources && \
  apt-get update && \
  apt-get install -y salt-common
