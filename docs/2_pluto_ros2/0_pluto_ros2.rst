Robotic Platform
================
This chapter will give a brief overview of the used Robotic Operating system and the reasons that led to the
chosen system components.

PLUTO uses **ROS2** (Robot Operating System) as a robotic platform as it provides a robust framework
for developing robot software and managing various components.
Combining a Raspberry Pi running ROS with a microcontroller running microROS is a common approach to build a
robot system with real-time capabilities and high-level control.
Communication between Microcontroller and ROS: To facilitate communication between the microcontroller running microROS
and the Raspberry Pi running ROS, ROS communication infrastructure allows the following options:

*   **ROS Topics:** You can publish and subscribe to ROS topics from both the Raspberry Pi and the microcontroller.
    Topics allow you to send and receive data between different parts of your robot. You can use ROS libraries for
    microcontrollers like rosserial or micro-ROS to set up communication.

*   **ROS Services:** Services in ROS allow you to call remote procedures on one device from the other.
    This is useful for requesting specific actions or services from your microcontroller.

*   **ROS Actions:** Actions provide a more flexible way to manage long-running tasks and feedback.
    Actions can be used when a more complex control over the robot's behavior is needed.
