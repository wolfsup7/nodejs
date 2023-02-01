FROM ubuntu:20.04@sha256:b33325a00c7c27b23ae48cf17d2c654e2c30812b35e7846c006389318f6a71c2

VOLUME /node

RUN buildDeps='binutils build-essential vim nasm git' \
  && apt-get update \
  && apt-get install -y --no-install-recommends --force-yes $buildDeps \
  && apt-get clean \
  && apt-get autoremove -y \
  && cpan install Text::Template \
  && rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/*

WORKDIR /node
