BuildA
===============
Build C/C++ AVR project.

## Image content

Image contains:

- gcc-avr
- gcc-avr-doc
- avr-libc
- avr-libc-doc
- binutils-avr
- avrdude
- avrdude-doc
- make
- cmake
- minicom

## Get image

```sh
docker pull osumaet/builda:1.0.0
```

## Usage

Run container from project's root. Project's folder will be mounted as volume to container.

Example for buulding and flash device on /dev/ttyUSB0
```sh
docker run --rm -it -i --device=/dev/ttyUSB0 -v .:/project builda:1.0.0 make
```
