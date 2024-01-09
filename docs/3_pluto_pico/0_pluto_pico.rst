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
     - | 4.90€
     - | `ebay <https://www.ebay.de/itm/115918606531?epid=22044590666&hash=item1afd4990c3:g:dMEAAOSw8URlJQnf&amdata=enc%3AAQAIAAAA4DcJlt4N%2BUo5ESF2nL6sEE1Z8vscSjs7rtdPV1rj7UPk3HQD7aX5ACOETRJOO8lguV3%2FsVuf1NKyFjaZP77u65yKwB7AdVG7%2FBi9%2F07w4wZzk18RhgFCwmH9W7DuQZZ9cxFRnVEVL7aP6R%2Flp8KYHOenVIyUVrrfJe2Askh9J%2BnvnbyhYWYuS3xMYc0kvNf3HELsAXFBSlQLxToXs5sSlYTN16pJC1fqdfoSx3XUYPM3nLwJEwWOkuwZKGkmxXhgPIgK67hBaiDgXvH%2F9aFdxeBLKVDZwpsZrWgFX8DAFi6N%7Ctkp%3ABk9SR4Cokt6dYw>`_
   * - | 8 channel relays
     - | 1
     - | 7.85€
     - | `ebay <https://www.ebay.de/itm/255283290288?_trkparms=amclksrc%3DITM%26aid%3D1110006%26algo%3DHOMESPLICE.SIM%26ao%3D1%26asc%3D20230804085259%26meid%3D3cc84dd01340425396b0fad0b22eec94%26pid%3D101195%26rk%3D2%26rkt%3D12%26sd%3D262499095094%26itm%3D255283290288%26pmt%3D1%26noa%3D0%26pg%3D4429486%26algv%3DSimPLWebV1EmbeddedAuctionsCPCAuto&_trksid=p4429486.c101195.m1851&amdata=cksum%3A2552832902883cc84dd01340425396b0fad0b22eec94%7Cenc%3AAQAIAAABEKQWTaSuKxcpq1j5hG%252Bz9F%252B8zK5%252FOpV48i2l8raehpQfnQ5X0AU9EGQjixlmPSYko2wwpYOChaX%252B4yLbiiEed6dOtVjRM6XBFiiCIgoNowo3YwdWfu5u4cl6ayhkqBbpuFmRE2hzR5GK25waek05ETCwlEI0bCcWt3%252BwojF7NmvVNmJxebAsnfTIT1pRegzYUfOg8F3XDdshZnw402mcf%252B1cMNa9dFizJDMPLG2A9TD59UUQAhrauQ2I4KPTuWuUsnetH89cmfzObxbaPEfO49M2kj446g0mPNxuJGwCOdalslyMu6O6qgqSX4chYSB4HuKn2PgzQoVyGaD8WAkPpPzb%252FQZdsq3%252B8WGOXe1aE4I%252F%7Campid%3APL_CLK%7Cclp%3A4429486&epid=6055142329>`_
   * - | MDD10A dual motor driver
     - | 1
     - | 23.90€
     - | `cytron <https://botland.de/dc-motortreiber/15818-cytron-mdd10a-zweikanaltreiber-fur-dc-30v-10a-motoren-5904422350444.html>`_
   * - | NEO 6M GPS module
     - | 1
     - | 6.90€
     - | `berrybase <https://www.berrybase.de/u-blox-neo-6m-gps-ttl-empfaenger-inkl.-antenne>`_
   * - | VL53L0X distance sensor
     - | 4
     - | 7.49€
     - | `az-delivery <https://www.az-delivery.de/products/vl53l0x-time-of-flight-tof-laser-abstandssensor?variant=32344531370080>`_
   * - | MCP9808 temperature sensor
     - | 8
     - | 5.90€
     - | `berrybase <https://www.berrybase.de/adafruit-mcp9808-hochpraezisions-i2c-temperatur-sensor-breakout-board>`_
   * - | HMC5883L compass sensor
     - | 1
     - | 4.45€
     - | `ebay <https://www.ebay.de/itm/255283194246?hash=item3b70106986:g:uSEAAOSwpYxb4K-E>`_
   * - | Sum Pluto-Pico
     - | 1
     - | 125.16€
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
