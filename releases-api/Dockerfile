FROM clojure:openjdk-11-tools-deps-1.10.1.739
LABEL maintainer="dave.yarwood@gmail.com"

USER root

# Install Datadog agent using the step-by-step Debian instructions here:
#
# https://app.datadoghq.com/signup/agent#debian
#
# NOTE: For security reasons, configuration of the Datadog agent is done at
# runtime.
RUN apt-get update
RUN apt-get install apt-transport-https
RUN echo 'deb https://apt.datadoghq.com/ stable 7' \
  > /etc/apt/sources.list.d/datadog.list
RUN apt-key adv --recv-keys \
  --keyserver hkp://keyserver.ubuntu.com:80 \
  A2923DFF56EDA6E76E55E492D3A80E30382E94DE
RUN apt-get update
RUN apt-get install datadog-agent
