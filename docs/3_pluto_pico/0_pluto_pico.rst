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

System
------

.. image:: pluto_pico-Connections.drawio.svg
  :width: 400
  :alt: Overview pluto_pico

.. list-table:: Pluto-pico parts functions
   :widths: 25 10 10 50
   :header-rows: 1

   * - Functional component
     - Amount
     - Positioning
     - Function
   * - | Relay
     - | 8 (on one PCB)
     - | No special needs
       | Please review datasheet
       | for dimensions
     - | Switches various
       | electrical loads. Such as:
       | Lights, Fan, beer-cooler
   * - | Motordriver
     - | 2 (on one PCB)
     - | No special needs
       | Please review datasheet
       | for dimensions
     - | Controls motor speed
       | of each motor
       | (left & right)
       | Defines speed &
       | direction of Pluto
   * - | Distance sensor
     - | 4
     - | Positioned at each
       | chain track (one in front,
       | one in the back)
       | Please review datasheet
       | for dimensions and specs
       | special requirements to
       | visual area apply!
     - | Measures distances
       | of each chain
       | to obstacle of that chain
       | Will act as a part of
       | safety concept to stop
       | Pluto if an movement
       | is not possible.
   * - | GPS
     - | 1
     - | Consists of antenna
       | and module
       | Antenna needs to be
       | flat and exposed to sky
     - | Determines current
       | position and speed
       | of Pluto
   * - | Orientation
     - | 1
     - | Needs to be away of
       | any magnets and flat
     - | Determines current
       | orientation &
       | acceleration of Pluto
   * - | Temperature sensor
     - | 3
     - | Needs to be at
       | location of
       | temperature
       | measurement
     - | Determines current
       | temperature of:
       | Battery cells, pluto-ros2
       | or Beer
   * - | Battery cell measurement
     - | 4
     - | No special needs
     - | Monitoring voltage
       | of battery cells
   * - | Emergency Switch
     - | 1
     - | Needs to be reachable
       | for Pluto users
     - | Emergency switch to
       | turn OFF PLuto at any
       | moment

.. image:: pluto_prototype_Steckplatine.png
  :width: 400
  :alt: Steckplatine pluto_pico

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
.. include:: 5_pluto_pico_proximity.rst
