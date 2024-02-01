Working with Pluto_pico
-----------------------

Introduction
~~~~~~~~~~~~
Pluto_pico simplifies the process of developing embedded applications, allowing developers to focus on higher-level
functionality.
Designed specifically for the Raspberry Pi Pico, it leverages the capabilities of the RP2040 microcontroller to provide
a robust and versatile platform for robotics and other embedded projects.

Prerequisites
~~~~~~~~~~~~~
Before beginning, ensure you have the following:

- A Raspberry Pi Pico with an RP2040 microcontroller
- A USB cable compatible with the Raspberry Pi Pico
- The ``zephyr.uf2`` file specific to the Pluto_pico project

Flashing Pluto_pico
~~~~~~~~~~~~~~~~~~~

1. **Prepare the Hardware**: Connect the Raspberry Pi Pico to your host PC using the USB cable. Ensure that you hold
down the BOOTSEL button on the Pico while connecting.

2. **Enter Mass Storage Mode**: Once connected, release the BOOTSEL button. Your Raspberry Pi Pico will now operate as
a mass storage device.

3. **Flash the Firmware**: Drag and drop the ``zephyr.uf2`` file onto the Raspberry Pi Pico drive. This process will
flash the firmware to the Pico's internal flash storage. This step is necessary once for each version of the firmware.

Using the Pico-Shell (version >= v0.1.0)
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~

1. **Establish a Serial Connection**:

   - To interact with Pluto_pico using the pico-shell, a serial port connection is required.
   - You can use a terminal program like PuTTY or minicom on your PC to connect to the serial port.
     The specific port can be found in your system's device manager (for Windows) or ``/dev`` directory
     (for Linux and macOS).
   - Select a baudrate of 115200 in your terminal program.

2. **Verify the Connection**:

   - Once connected, the onboard LED on the Raspberry Pi Pico will start flashing at a frequency of 1 second.
     This indicates a successful serial connection.

3. **Using Pico-Shell**:

   - Once connected via the terminal program, you can interact with the Pluto_pico through various commands.
   - The pico-shell allows you to configure and control external peripherals, read sensor data, and manage the
     robot's operations. Try one of the commands from the following table.

Command Overview
~~~~~~~~~~~~~~~~
The following table contains in short all available commands.

Explore the detailed command list and examples provided in the subsequent sections to fully utilize the capabilities of
Pluto_pico.

Happy developing!

.. list-table:: Pluto Protocol
   :widths: 25 50 50
   :header-rows: 1

   * - Command
     - Description
     - Supported Arguments
   * - :code:`ANY_COMMAND`
     - | Calling without arguments:
       | Detailed info about command
       | only excpetion: :code:`version`
     - | :code:`--help`
       | short info about command
   * - :code:`echo`
     - | returns <message>
       | **pluto-pico version:** >= v0.1.0
     - | :code:`<message>`
       | respond with message
   * - :code:`version`
     - | returns pluto-pico version
       | no argument := APP_VERSION_STRING
       | **pluto-pico version:** >= v0.1.0
     - | :code:`--build-ver`
       | APP_BUILD_VERSION
   * - :code:`relays`
     - | control relays of pluto-pico
       | **pluto-pico version:** >= v0.1.0
     - | :code:`--set-bytes <value[0..0xFF]>`
       | :code:`--set-relay <name> <state[0||1]>`
       | :code:`--list-relays`
       | **pluto-pico version:** >= v0.2.0:
       | :code:`--get-relay <name>`
   * - :code:`motor1`
     - | control motor1 of pluto-pico
       | **pluto-pico version:** >= v0.3.0
     - | :code:`set-dir <state[0||1]>`
       | :code:`set-speed <value[0..100]>`
       | (unsafe) :code:`Zset-speed <value[0..100]>`
       | :code:`get-speed`
       | :code:`get-dir`
       | :code:`get-motor`
       | :code:`config-acc-rate <value[0..100]>`
       | :code:`config-brak-rate <value[0..100]>`
       | :code:`config-acc-rate-delay <value[0..0xFFFF]ms>`
       | :code:`config-brak-rate-delay <value[0..0xFFFF]ms>`
   * - :code:`motor2`
     - | control motor2 of pluto-pico
       | **pluto-pico version:** >= v0.3.0
     - | :code:`set-dir <state[0||1]>`
       | :code:`set-speed <value[0..100]>`
       | (unsafe) :code:`Zset-speed <value[0..100]>`
       | :code:`get-speed`
       | :code:`get-dir`
       | :code:`get-motor`
       | :code:`config-acc-rate <value[0..100]>`
       | :code:`config-brak-rate <value[0..100]>`
       | :code:`config-acc-rate-delay <value[0..0xFFFF]ms>`
       | :code:`config-brak-rate-delay <value[0..0xFFFF]ms>`
   * - :code:`motors`
     - | control motors of pluto-pico at once
       | **pluto-pico version:** >= v0.4.0
     - | :code:`set <speed_m1[0..100]> <dir_m1[0||1]> <speed_m2[0..100]> <dir_m2[0||1]>`
