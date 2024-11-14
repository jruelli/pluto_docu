Tutorial: Setting up pluto-pico:
--------------------------------

Flashing pluto-pico firmware
~~~~~~~~~~~~~~~~~~~~~~~~~~~~
Get yourself a raspberry-pico and a Micro-USB cable that can be used for USB-based communication.
Push the Button and while keep pushing connect the raspberry-pico with your pc.
After connecting to the pc you can release the button.
The raspberry-pico should now be visible as a mass-storage-device.
Now go to the pluto-pico repository and download the artefacts. (https://gitlab.com/pluto-ipek/pluto_pico/-/jobs)
Flash the uf2 file onto the raspberry-pico by dragging the file to the raspberry-pico mass-storage-device.

You know that this step was successful if the raspberry-pico starts blinking the led.

Get a serial connection with raspberry-pico
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~
After flashing your firmware you can get a serial connection and start communicating with the raspberry-pico.
You need to download a program for serial connection. This example will show you how to set up
MobaXTerm but there are multiple alternatives that work in the same way.
Open MobaXterm. Select New Connection -> Serial Connection.
As a baudrate you can chose 115200 (pluto-pico will automatically adjust to a lower baudrate if chosen)
Select your Com-port.
Click Accept. You are done.

Talking with pluto-pico
~~~~~~~~~~~~~~~~~~~~~~~
Congratulations, you are almost done! Now it's time to communicate with pluto-pico.
Commands can be used to interact with sensors and actuators.
Depending on the version various commands are available.

Please don't hesitate to play around with various commands.
That's what these commands were made for. :-)

All commands have a common rule-set:

* All commands are safe to use. No hardware can be destroyed when putting in commands.
  Exceptions are actuators, so motors and relays. Please take care when using those and go through
  the in-depth explanation of them before using them.
* All commands have help subcommands. Any command and even any subcommand can be called with a "--help" parameter.
* All commands/configuration are volatile. The configuration is lost when the raspberry-pico is power-cycled.
* If a permanent configuration is desired please have a look at pluto-control.
* Using <Tab> to autocomplete and <Arrow-up> for previous commands improves usability
* In-depth documentation of commands can be found in: **TODO**

Example interactions
~~~~~~~~~~~~~~~~~~~~

Example I: Call the version of pluto-pico

.. code-block:: console

    version --help
    # Response:
    # App version
    version
    # Response: 1.0.0

Example II: Configure and control motor1

.. code-block:: console

    # Step 1: Check current motor configuration
    motor1 get-motor

    # Response:
    # name: Pluto Motor
    # direction: 0
    # speed: 0
    # acceleration_rate: 50
    # acceleration_rate_delay: 300ms
    # braking_rate: 40
    # braking_rate_delay: 200ms

    # Step 2: Set motor direction to 1
    motor1 set-dir 1

    # Step 3: Set motor speed to 60%
    motor1 set-speed 60

    # Step 4: Configure acceleration and braking rates
    motor1 config-acc-rate 70
    motor1 config-brak-rate 50

    # Step 5: Set acceleration and braking delays
    motor1 config-acc-rate-delay 400
    motor1 config-brak-rate-delay 200

    # Step 6: Verify settings
    motor1 get-motor

    # Response:
    # name: Pluto Motor
    # direction: 1
    # speed: 60
    # acceleration_rate: 70
    # acceleration_rate_delay: 400ms
    # braking_rate: 50
    # braking_rate_delay: 200ms

Example III: Configure safety-critical sensor

.. code-block:: console

    # Step 1 (Optional): Asking functionality of em_btn config-mode
    em_btn config-mode --help
    # Response:
    # Enable(1)/disable(0) motor stop on emergency button press.
    # Step 2: Enabling safety functionality for Emergency_button
    em_btn config-mode 1
    # Step 3 (Optional): Asking sensor value from em_btn
    em_btn get
    # Response
    # 1
