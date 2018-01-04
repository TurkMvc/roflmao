# roflmao

[![Build Status (Travis-CI)](https://travis-ci.org/lolengine/lol-roflmao.svg?branch=master)](https://travis-ci.org/lolengine/lol-roflmao)
[![Build Status (Semaphore-CI)](https://semaphoreci.com/api/v1/samhocevar/lol-roflmao/branches/master/badge.svg)](https://semaphoreci.com/samhocevar/lol-roflmao)

`roflmao` is a simple project using Lol Engine. If you want to get
started with Lol Engine, you may either:

 - fork this project
 - duplicate this project (see [“duplicating a repository”](https://help.github.com/articles/duplicating-a-repository/))

## Setup

Make sure Lol Engine and its submodules are properly initialised:

    git submodule update --init --recursive

On Linux, make sure the following packages are installed:

    automake autoconf libtool pkg-config

## Activate optional subsystems

You can edit `build.config` to activate some subsystems:

  - OpenGL (requires `libglew-dev`)
  - SDL (requires `libsdl2-dev libsdl2-image-dev libsdl2-mixer-dev`)
  - FFmpeg
  - Imlib2
  - libPNG

## Configure

The default application is called `roflmao` and lies in the `src` subdirectory.
You should rename it to whatever your application will be called. Make sure
to modify the following files:

    src/roflmao.cpp
    configure.ac (Linux/Unix)
    Makefile.am (Linux/Unix)
    src/Makefile.am (Linux/Unix)
    roflmao.sln (Windows)
    src/roflmao.vcxproj (Windows)

You can of course have several projects in the same repository.

## Build

Then bootstrap the project and configure it:

    ./bootstrap
    ./configure

Finally, build the project:

    make

