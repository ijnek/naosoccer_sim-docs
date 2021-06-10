.. _development-statuses:

Development Statuses
####################

The project is still under development. Details on what is ready and what is not ready to be used,
is listed below.

The project **can currently be used** for:

* Launching an agent and connecting to a running instance of rcssserver3d
* Sending Joint effector commands for all joints
* Receiving the following sensory data; Joint Angles, Buttons, Accelerometer, Gyroscope, Angle
* Receiving the following vision data; Ball, Goalposts, FieldLines, Robots, Corner Flags
* Simulating button presses through a Button Simulator

It **cannot be used yet** for:

* Receiving the following sensory data; Sonar, FSR, Touch, Battery
* Receiving the following vision data; Field Features
* Receiving the following joint sensory information; temperature, current, stiffness
* Specifying stiffness in joint effector comamnds
* Sending eye led commands
