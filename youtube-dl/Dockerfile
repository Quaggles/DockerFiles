#
# Dockerfile for youtube-dl
#

FROM alpine
MAINTAINER ryan <noreply@easypi.pro>

RUN set -xe \
    && apk update \
    && apk add --no-cache ca-certificates \
                          ffmpeg \
                          openssl \
                          python3 \
                          aria2 \
    && python3 -m pip install --upgrade pip \
    && pip3 install youtube-dl

WORKDIR /data

ENTRYPOINT ["youtube-dl"]
CMD ["--help"]
