stm32-toolchain-builder
=======================

stm32-toolchain-builder is a build script of arm-gcc toolchain for the development targeting STM32 microcontrollers.

Features:
  - Brand new GCC toolchain (gcc-4.8.1)
  - Multilib available for Cortex-M0,M3,M4
  - You only have to do is to execute "make" (see the usage below)

Version
-------

0.1.0

Usage
-----

For Ubuntu 13.04 railing:
```bash
$ sudo apt-get install g++ autoconf texinfo gcc-multilib g++-multilib libncurses5-dev
$ git clone https://github.com/tokoro10g/stm32-toolchain-builder
$ cd stm32-toolchain-builder
$ make && sudo make install
```

For other distributions or versions, you may need some more packages to build.

If you got some errors, install the needed packages, then type:
```bash
$ make distclean
$ make && sudo make install
```
or 
```bash
$ make build
```
The former cleans up the working directory, then builds.
The latter does not download tarballs or extract them; just build.

Changing mirror site for tarballs
---------------------------------

List of the URL of tarballs are written at `packagelist` file.
You can modify this to select mirror sites.


Make targets
------------

- `all`

 default configuration.
 
 processes all targets except for `build-pdf`.

- `get-packages`

 downloads tarballs.

- `extract`

 extracts tarballs.

- `patch`

 patches some files for build.

- `build`

 processes all "build" targets 

- `build-expat`

 builds expat.

- `build-zlib`

 builds zlib.

- `build-gmp`

 builds gmp.

- `build-mpfr`

 builds mpfr.

- `build-mpc`

 builds mpc.

- `build-binutils`

 builds binutils.

- `build-gcc-1`

 builds gcc first pass.

- `build-newlib`

 builds newlib

- `build-gcc-2`

 builds gcc second pass.

- `build-gdb`

 builds gdb.

- `strip`

 strips some binary files.

- `build-pdf`

 produces documentations. (disabled by default)


Versions
--------
- binutils: 2.23.2
- gcc: 4.8.1
- newlib: 1.20.0
- gdb: 7.6.1
- gmp: 5.1.2
- mpfr: 3.1.2
- expat: 2.1.0
- zlib: 1.2.8
- mpc: 1.0.1


License
-------

GNU GPL v3.0

http://www.gnu.org/licenses/gpl-3.0.txt

