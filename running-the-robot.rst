Running the Robot
#################

This is a tutorial on how to launch a simulated NAO robot in the SimSpark simulator using ROS2.

.. attention::

    This tutorial assumes that you have set up rcssserver3d on your computer. If you haven't done so already,
    go to `SimSpark's Gitlab`_ and follow the installation instructions.

.. attention::

    This tutorial assumes that you have built the packages in this repository and have sourced the setup file
    for the workspace you are in.

Starting rcsoccersim3d
**********************

In a terminal, start the simulator by running:

.. code-block:: console

    rcsoccersim3d
    

.. warning::

    Simulator tends to crash sometimes when connecting / disconnecting agents, which leaves unwanted
    server processes lingering. To kill this process, run ``pkill -9 rcssserver3d`` before restarting
    the simulation server.

Starting rcss3d_agent node
**************************

In a new terminal, run:

.. code-block:: console

    ros2 run rcss3d_agent rcss3d_agent

You should see your robot in the rcssmonitor3d:

.. image:: images/screenshot.png


List Publishing/Subscribed Topics
*********************************

In a new terminal, run:

.. code-block:: console

    ros2 topic list

A list of topics that the node is subscribed to or publishing will show up:

.. code-block:: console

    /effectors/joints
    /parameter_events
    /rosout
    /sensors/accelerometer
    /sensors/angle
    /sensors/buttons
    /sensors/fsr
    /sensors/gyroscope
    /sensors/joints
    /sensors/sonar
    /sensors/touch
    /vision/ball


.. _SimSpark's Gitlab: https://gitlab.com/robocup-sim/SimSpark/-/wikis/home