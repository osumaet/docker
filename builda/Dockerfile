FROM alpine:3.18.4

RUN apk update && \
    apk upgrade && \
    apk --no-cache add \
        make \
        cmake \
        minicom \
        gcc-avr-doc \
        gcc-avr \
        avr-libc-doc \
        avr-libc \
        binutils-avr \
        avrdude-doc \
        avrdude

VOLUME [ "/project" ]
WORKDIR /project
