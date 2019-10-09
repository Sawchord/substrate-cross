FROM rustembedded/cross:armv7-unknown-linux-gnueabihf-0.1.16

RUN apt-get update && apt-get install -y gcc-arm-linux-gnueabihf g++-arm-linux-gnueabihf libc6-dev-armhf-cross libclang-dev

# This is needed for bindgen to pull the correct stdlib
ENV CPATH=/usr/arm-linux-gnueabihf/include