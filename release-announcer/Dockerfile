FROM circleci/buildpack-deps:bionic
LABEL maintainer="dave.yarwood@gmail.com"

USER root

# Install requirements for `announce-release` script
RUN apt update && apt install -y jo

USER circleci

