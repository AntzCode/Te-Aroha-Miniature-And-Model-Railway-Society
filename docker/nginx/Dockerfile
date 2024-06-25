FROM jwilder/nginx-proxy

# File Author / Maintainer
LABEL org.opencontainers.image.authors="AntzCode Ltd <www.antzcode.com>"

EXPOSE 80
EXPOSE 443

# Let it install without stopping for user input
ARG DEBIAN_FRONTEND=noninteractive

# Update the repository sources list
RUN apt-get update

# Include server admin tools
RUN apt-get install -y nano htop ncdu git curl


