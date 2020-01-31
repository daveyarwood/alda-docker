FROM circleci/openjdk:8-jdk
LABEL maintainer="dave.yarwood@gmail.com"

USER root

# Install envsubst (used to generate the launch4j XML config file)
RUN apt update && apt install -y gettext-base

# Install launch4j
WORKDIR /home/circleci
RUN wget -O launch4j.tar.gz \
      https://sourceforge.net/projects/launch4j/files/launch4j-3/3.12/launch4j-3.12-linux-x64.tgz/download \
      && tar xzvf launch4j.tar.gz
ENV PATH="/home/circleci/launch4j:${PATH}"

USER circleci

