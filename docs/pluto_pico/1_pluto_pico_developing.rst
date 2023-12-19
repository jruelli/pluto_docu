Developing Pluto_pico
---------------------
Pluto_pico is based on zephyr.
Please refer to the repo here: https://gitlab.com/pluto_ipek/pluto_pico

To start please refer to the Installation of zephyr.
https://docs.zephyrproject.org/latest/develop/getting_started/index.html

It is necessary to install any dependencies, zephyr and the zephyr sdk.
We highly recommend to test zephyr and get some understanding by building the blinky example.
Following the zephyr tutorial the blinky example for the raspberry_pico can be built via:

:code:`west build -p always -b rpi_pico samples\basic\blinky`

External pin mapping on the Pico W is identical to the Pico, but note that internal RP2040 GPIO lines 23, 24, 25, and 29
are routed to the Infineon module on the W. Since GPIO 25 is routed to the on-board LED on the Pico, but to the Infineon
module on the Pico W, the "blinky" sample program does not work on the W (use hello_world for a simple test program
instead).
For more information about the Raspberry Pico in zephyr please visit:
https://docs.zephyrproject.org/latest/boards/arm/rpi_pico/doc/index.html

After the installation is complete and verified the project can be cloned locally.

When opening the project with an IDE such as CLion the IDE will ask for the CMake target.
Chose Build Type **Default** and leave everything else as it is.
The application will find zephyr and any dependencies on its own.

After the CMake build has finished several targets are available to build.
The default target "zephy_final" will build the pico application.
The relevant binary for the raspberry_pico will be the zephyr.uf2.
