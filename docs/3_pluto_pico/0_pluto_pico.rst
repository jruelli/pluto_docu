Pluto Pico
================
We noticed that in previous groups the project was lacking embedded software developers.
Each group always started their project by running motors from scratch.
In order for the project to grow each year this needs to stop!

That's why pluto-pico exists. Pluto-pico encapsulates any embedded software part and to make it easy to use and most
suitable for pluto and its future developers.

Pluto can be used independently to any system. All it needs is a USB host in order to connect to the pluto-shell.
That can be a raspberry pi but also any kind of computer.

Pluto-pico is also cheap since it runs on a 7.50€ raspberry-pico making so it is possible for for any project
participant to have one pluto-pico to test and verify.

Pluto-shell provides a user-friendly and easy to use interface to test motordrivers or sensors that are used for Pluto.

Since the application has been developed as a zephyr application it is also possible to exchange the microcontroller or
do any changes on the embedded part.

Overview
--------

.. image:: pluto_pico-Connections.drawio.svg
  :width: 400
  :alt: Overview pluto_pico

System
------

.. list-table:: Pluto-pico parts
   :widths: 25 10 10 50
   :header-rows: 1

   * - Part
     - Amount
     - Price per Unit
     - Sources
   * - | Raspberry Pi Pico
     - | 1
     - | 7.49€
     - | `Raspberry Pi pico <https://www.az-delivery.de/en/products/raspberry-pi-pico>`_
   * - | 8 channel relays
     - | 1
     - | 12.99€
     - | `8 channel relay <https://www.az-delivery.de/en/products/8-relais-modul>`_
   * - | MDD10A dual motor driver
     - | 1
     - | 23.90€
     - | `cytron-mdd10a <https://botland.de/dc-motortreiber/15818-cytron-mdd10a-zweikanaltreiber-fur-dc-30v-10a-motoren-5904422350444.html>`_
   * - | NEO 6M GPS module
     - | 1
     - | 6.90€
     - | `neo-6m-gps <https://www.berrybase.de/u-blox-neo-6m-gps-ttl-empfaenger-inkl.-antenne>`_
   * - | VL53L0X
     - | 2
     - | 7.49€
     - | `vl53l0x <https://www.az-delivery.de/products/vl53l0x-time-of-flight-tof-laser-abstandssensor?variant=32344531370080>`_
   * - | Sum Pluto-Pico
     - | 1
     - | 66.26€
     - |

Microcontroller
~~~~~~~~~~~~~~~

Pluto_pico uses the Raspberry Pi Pico microcontroller. To communicate with pluto-pico use the pluto-shell.
Simply connect a usb-cable to and open a serial connection. A list of supported commands can be found in the table below.

.. image:: pico-pinout.svg
  :width: 400
  :alt: available connections for pluto_pico

.. include:: 1_pluto_working_with_pico.rst
.. include:: 2_pluto_pico_developing.rst
.. include:: 3_pluto_pico_relays.rst
.. include:: 4_pluto_pico_motors.rst
