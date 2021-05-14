.. _development-statuses:

Development Statuses
####################

The project is still under development. Details on what is ready and what is not ready to be used,
is listed below.

The project **can currently be used** for:

* Launching an agent in a running instance of rcssserver3d
* Sending Joint effector commands for all joints
* Receiving the following sensory data; Joint Angles, Buttons, Accelerometer, Gyroscope, Angle
* Receiving the following vision data; Ball
* Simulating button presses through a CLI, similar to turtlebot3_teleop, from the ROS tutorials.
* Converting nao-specific joint angle data to ROS-standard joint state data (`sensor_msgs/msg/JointState`_)

It **cannot be used yet** for:

* Receiving the following sensory data; Sonar, FSR, Touch, Battery
* Receiving the following vision data; Field Features, Lines, Robots, Goals
* Receiving the following joint sensory information; temperature, current, stiffness
* Specifying stiffness in joint effector comamnds
* Sending eye led commands

.. _sensor_msgs/msg/JointState: http://docs.ros.org/en/melodic/api/sensor_msgs/html/msg/JointState.html