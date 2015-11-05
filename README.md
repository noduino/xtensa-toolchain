Xtensa-Toolchain
==================================================================
Toolchain for supporting the Xtensa architecture (e.g. ESP8266 WiFi SoC)

Xtensa lx106 architecture toolchain, based on following projects:

- https://github.com/jcmvbkbc/crosstool-NG
- https://github.com/jcmvbkbc/gcc-xtensa
- https://github.com/jcmvbkbc/newlib-xtensa
- https://github.com/tommie/lx106-hal
- https://github.com/igrr/esptool-ck
- https://github.com/igrr/mkspiffs


## Generating from prebuilt package

```
$ git clone git://github.com/icamgo/xtensa-toolchain.git xtensa-toolchain
$ cd xtensa-toolchain/release
$ make win32					# build the toolchain used in windows
$ make linux32					# build the toolchain used in 32bit linux
$ make linux64					# build the toolchain used in 64bit linux
$ make osx						# build the toolchain used in Mac OS X
```
