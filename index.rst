.. naosoccer_sim documentation master file, created by
   sphinx-quickstart on Thu May  6 11:28:46 2021.
   You can adapt this file completely to your liking, but it should at least
   contain the root `toctree` directive.

Welcome to naosoccer_sim's documentation!
=========================================

This set of packages allow you to launch a soccer player in the rcssserver3d soccer simulation, 
and send commands and receive sensory data as if you are interacting with a physical NAO robot.

The set of packages are under development, and **can currently be used for**:

* Launching an agent in a running instance of rcssserver3d
* Sending Joint effector commands for all joints
* Receiving the following sensory data; Joint Angles, Buttons, Accelerometer, Gyroscope, Angle
* Receiving the following vision data; Ball
* Simulating button presses through a CLI, similar to turtlebot3_teleop, from the ROS tutorials.
* Converting nao-specific joint angle data to ROS-standard joint state data (`sensor_msgs/msg/JointState`_)

It **cannot** be used yet for:

* Receiving the following sensory data; Sonar, FSR, Touch, Battery
* Receiving the following vision data; Field Features, Lines, Robots, Goals
* Receiving the following joint sensory information; temperature, current, stiffness
* Specifying stiffness in joint effector comamnds
* Sending eye led commands

.. toctree::
   :maxdepth: 2
   :caption: Contents:

   tutorial
   rcss3d_agent
   joints_to_joint_state
   nao_buttons_sim
   naosoccer_sim_launch




Indices and tables
==================

* :ref:`genindex`
* :ref:`modindex`
* :ref:`search`


.. _sensor_msgs/msg/JointState: http://docs.ros.org/en/melodic/api/sensor_msgs/html/msg/JointState.html