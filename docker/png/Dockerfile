FROM alpine:3.7

MAINTAINER Arigoldy <contact@arigoldy.com>

RUN apk add --no-cache pngquant

RUN set -x ; \
  addgroup -g 82 -S www-data ; \
  adduser -u 82 -D -S -G www-data www-data && exit 0 ; exit 1

RUN mkdir /var/workdir && chown www-data:www-data /var/workdir

COPY docker/png/scripts/entrypoint.sh /
RUN chmod +x /entrypoint.sh

USER www-data
WORKDIR /var/workdir

ENTRYPOINT ["/entrypoint.sh"]
CMD ["--help"]