Pluto_Control
==========
Pluto_control is a software application for configuring & controlling
the robot's sensors & actors. Furthermore it communicates with the customer
over firebase.

Pluto_Control is a python based application that can run on many different OS.
Still there are requirements that need to be fulfilled in order for it to run.

Hardware-based requirements:

- Graphical User Interface (Screen/keyboard): On a raspberry-pi this can be accomplished via VNC.
- Internet Access: Pluto_control expects a working Internet Access (for Firebase)
- USB-Interface for Pluto-pico
- Nice-to-have: If control shall be done via controller controller must be connected outside of pluto-control

Software-based requirements:

- Python3
- From pluto_control's requirement list
-
- (For devices without GUI): SSH Access, VNC Access
