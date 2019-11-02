# tvp
## A GameBoy Emuator

---

[![CircleCI](https://circleci.com/gh/venkat24/tvp/tree/master.svg?style=svg&circle-token=0915c0ed7c3b36f5aed8ddcd1b659547c662088c)](https://circleci.com/gh/venkat24/tvp/tree/master)

<h1 align="center">
    <img src="https://github.com/venkat24/tvp/blob/master/images/start.png" width="300"/>
    <img src="https://github.com/venkat24/tvp/blob/master/images/tetris.png" width="300"/><br />
</h1>

This is an incomplete, experimental Nintendo GameBoy emulator written in C++. It runs Tetris!

## Build and Install Instructions :

### Linux

1. Install CMake (> 3.5.1)
        On Ubuntu, run `apt install cmake`
        Otherwise, you can download the binaries from [cmake.org/download](https://cmake.org/download/)

2. Install SFML
        On Ubuntu, run `apt install libsfml-dev`
        Otherwise, download / build the library from [sfml-dev.org](https://www.sfml-dev.org/)

3. Clone the project and run
`mkdir build && cd build`

4. `cmake .. -DCMAKE_INSTALL_PREFIX=<path_to_someplace_to_install> -DCMAKE_BUILD_TYPE=Release`
        You can skip the `CMAKE_BUILD_TYPE` flag (or set it to `Debug`) if you want to run unit tests.

5. `make install`

6. `cd <path_to_someplace_to_install>/bin`

7. `./tvp /path/to/rom_file.gb`

8. Enjoy your game! Use the WASD keys as the GameBoy DPad. Use K, L, Backspace, and Enter keys as A, B, SELECT, and START buttons.

### Windows

You can build and run tvp in Visual Studio. Open the repo as a folder from Visual Studio 2017 or above, and it should automatically configure CMake.

1. Install [CMake](https://cmake.org/download/)

2. Download the [SFML SDK](https://www.sfml-dev.org/download/sfml/2.5.1/),
    If Visual Studio cannot find SFML, manually set the `SFML_ROOT` CMake variable to wherever you downloaded the SDK. You can pass this as a command line argument in the run settings with `-DSFML_ROOT=<path>`. 

3. Click `Build All` from the CMake menu.

4. Select `tvp.exe` as your launch item. You can edit the launch item properties to set command line arguments.

5. Enjoy your game! Use the WASD keys as the GameBoy DPad. Use K, L, Backspace, and Enter keys as A, B, SELECT, and START buttons.