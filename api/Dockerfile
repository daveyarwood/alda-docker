FROM clojure:openjdk-17-tools-deps-1.11.1.1113
LABEL maintainer="dave.yarwood@gmail.com"

USER root

RUN apt update && apt install -y curl

# Install Datadog agent using the instructions here (but without exposing the
# API key here):
#
# https://app.datadoghq.com/signup/agent#debian
#
# NOTE: For security reasons, configuration of the Datadog agent is done at
# runtime.
RUN \
  DD_INSTALL_ONLY="true" \
  DD_API_KEY="placeholder" \
  DD_SITE="datadoghq.com" \
  bash \
  -c "$(curl -L https://s3.amazonaws.com/dd-agent/scripts/install_script_agent7.sh)"
