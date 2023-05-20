# nn.h

Simple stb-style head-only library for Neural Networks. Created for educational purposes. Not suitable for production.

![thumbnail](./thumbnail.png)

## Quick Start

You need [meson](https://mesonbuild.com/Getting-meson.html) to compile this:


```console
$ meson setup build
$ meson compile -C build
$ ./build/img2nn ./mnist/training/8/10057.png ./mnist/training/6/10032.png
```

## Gym

Gym is a separate GUI app that uses nn.h to pre-train Neural Networks.

An example usage would be:
```console
$ meson setup build
$ meson compile -C build
$ ./build/adder_gen
$ ./build/gym adder.arch adder.mat
```

### Controls

|Keys|Description|
|---|---|
|<kbd>SPACE</kbd>|Toggle pause|
|<kbd>r</kbd>|Restart the training|
