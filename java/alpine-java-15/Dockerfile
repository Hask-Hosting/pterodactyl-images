FROM        doptopenjdk:15-jre-hotspot

LABEL       author="Linux123123" maintainer="linas.alexx@gmail.com"

RUN         apk add --update --no-cache ca-certificates curl fontconfig git openssl sqlite tar tzdata \
			    && adduser -D -h /home/container container

USER        container
ENV         USER=container HOME=/home/container
WORKDIR     /home/container

COPY        ./../entrypoint.sh /entrypoint.sh
CMD         [ "/bin/ash", "/entrypoint.sh" ]
