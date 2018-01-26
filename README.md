# Airwindows open-source VST plugins for Linux

This repository contains a CMake project that builds Airwindows plugins for
Linux. Thanks to the Patreon supporters, Chris now publishes some of his plugins
under the MIT license on his GitHub, thus making this possible. Please, consider
supporting him. More info:

1. <https://patreon.com/airwindows>
2. <https://github.com/airwindows/airwindows>
3. <http://airwindows.com>

## Building

Install CMake from your package manager:

- Debian / Ubuntu: `apt install cmake`
- Fedora / CentOS: `dnf install cmake`
- Arch / Manjaro: `pacman -S cmake`

To build the plugins you would need to grab the VST SDK and copy it to the
`include/vstsdk` directory. You need to do it yourself, because the Steinberg’s
license doesn’t allow to distribute their SDK with licenses other than GPL. You
can get it from the following page:
<https://www.steinberg.net/en/company/developers.html>. The structure of the
`include/vsdsdk` directory should be as follows:

```
include/vstsdk/
├── pluginterfaces
│   └── vst2.x
│       ├── aeffect.h
│       ├── aeffectx.h
│       └── vstfxstore.h
├── aeffeditor.h
├── audioeffect.cpp
├── audioeffect.h
├── audioeffectx.cpp
├── audioeffectx.h
├── CMakeLists.txt
└── vstplugmain.cpp
```

Then, navigate to the `build` directory and run `cmake .. && make`.

Copy the `.so` files wherever you would like.

