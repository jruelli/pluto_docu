Pluto Pico
================
This chapter will explain everything you need to know about Pluto_pico.

Overview
--------
We noticed that in previous groups the project was lacking embedded software developers.
That's why we tried to focus on a microcontroller that can be used independently.
This will give future teams the possibility to exchange parts of their system such as changing the pluto_ros or
the motor_driver part.

.. image:: pluto_pico-Overview.drawio.png
  :width: 400
  :alt: Pluto with highlighted pluto_pico

Microcontroller
---------------
Pluto_pico is an embedded microcontroller that will be used to control the motor_drivers.
Pluto_pico uses the Raspberry Pi Pico microcontroller.

.. image:: pico-pinout.svg
  :width: 400
  :alt: available connections for pluto_pico

Connections
-----------
Pluto_pico can be controlled via the usb interface. This will give other groups the opportunity to
test the motor drivers and to control the pluto_pico via a usb connection from
the Raspberry Pi or any other usb host.
The connection will use the pluto_protocol to interact with. More infos about the pluto_protocol can be found at the
chapter "Working with Pluto_pico"

The advantage of this system is additionally that it will be very easy for other teammembers to interact with the motors
in order to test and verify the drive system.

.. image:: pluto_pico-Connections.drawio.png
  :width: 400
  :alt: available connections for pluto_pico


.. include:: 1_pluto_working_with_pico.rst
.. include:: 2_pluto_pico_developing.rst
.. include:: 3_pluto_pico_relays.rst
