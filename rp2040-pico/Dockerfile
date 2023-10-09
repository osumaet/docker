FROM alpine:3.18.4
RUN apk update && \
    apk upgrade && \
    apk --no-cache add \
            cmake \
            make \
            gcc \
            g++ \
            build-base \
            python3 \
            py3-pip \
            libusb-dev \
            newlib-arm-none-eabi \
            gcc-arm-none-eabi \
            g++-arm-none-eabi \
            minicom \
            git \
            bsd-compat-headers
RUN mkdir /picotool-build && cd /picotool-build && git clone https://github.com/raspberrypi/pico-sdk.git && cd /picotool-build/pico-sdk && cmake . && make
RUN cd /picotool-build && export PICO_SDK_PATH=/picotool-build/pico-sdk && git clone https://github.com/raspberrypi/picotool && cd /picotool-build/picotool && cmake . && make && cp picotool /usr/bin
RUN rm -R /picotool-build
RUN apk del git bsd-compat-headers --quiet
ENV PICO_SDK_PATH=/pico-sdk
VOLUME [ "/project", "/pico-sdk" ]
WORKDIR /project

