ARG BASE_IMAGE=ubuntu:20.04
FROM ${BASE_IMAGE}

RUN apt-get update -q && apt-get upgrade -yq && apt-get install -yq wget gnupg jq curl git && \
	wget -q -O - https://packages.cloudfoundry.org/debian/cli.cloudfoundry.org.key | apt-key add - && \
	echo "deb https://packages.cloudfoundry.org/debian stable main" | tee /etc/apt/sources.list.d/cloudfoundry-cli.list  && \
	apt-get update -q && apt-get install -yq python3 cf-cli && apt-get clean && rm -rf /var/lib/apt/lists/*

