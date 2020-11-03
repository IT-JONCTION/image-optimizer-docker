FROM debian:latest

MAINTAINER Arigoldy <contact@arigoldy.com>

RUN apt-get update && apt-get install -y apt-utils jpegoptim --no-install-recommends && rm -r /var/lib/apt/lists/*

# Set up the application directory
VOLUME ["/app"]
WORKDIR /app

ENTRYPOINT ["jpegoptim"]
CMD [ "-h" ]