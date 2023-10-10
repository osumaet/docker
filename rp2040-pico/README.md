Build-RP2040
===============
Build C/C++ RP2040 project.

## Image content

Image contains:

- cmake
- make
- gcc
- g++
- python3
- gcc-arm-none-eabi
- g++-arm-none-eabi
- minicom

## Get image

```sh
docker pull osumaet/build-rp2040:1.0.0

## Usage example
Place Pico SDK at pico-sdk folder inside user's home. Then place examples to pico-examples. Next command will build blink.
```
docker run --rm -it \
 -v ~/pico-sdk:/pico-sdk \
 -v ~/pico-examples:/project \
 osumaet/build-rp2040:1.0.0 \
 sh -c 'mkdir -p build && cd build && cmake .. && make blink'
```