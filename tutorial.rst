Tutorial
########

.. attention::

    This tutorial assumes that you have set up rcssserver3d on your computer. If you haven't done so already,
    go to `SimSpark's Gitlab`_ and follow the installation instructions.

.. attention::

    This tutorial assumes that you have built the packages in this repository and have sourced the setup file
    for the workspace you are in.


Launching a soccer player
*************************

Starting rcssserver3d
=====================

In a terminal, run ``rcssserver3d`` to start the simulation server.

.. note::
    
    The simulation server must be started separately from this package.

.. warning::

    Simulation server tends to crash sometimes when connecting / disconnecting agents, which leaves unwanted
    server processes lingering. To kill this process, run ``pkill -9 rcssserver3d`` before starting
    the simulation server.

Starting rcss3d_agent node
==========================

In a new terminal, run ``ros2 run rcss3d_agent rcss3d_agent``.

List Publish/Subscribed Topics
==============================

In a new terminal, run ``ros2 topic list``. 
A list of topics that the node is subscribed to or publishing will show up.

.. code-block:: bash

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



Simulating Button Presses
*************************

In a new terminal, run ``ros2 run nao_button_sim nao_button_sim``.

To simulate a button press, click on a key specified in the assigned keys list below.

.. code-block:: bash

    ---------  Assigned Keys  ---------                                 
    G - Chest button
    C - Left Foot Bumper Left
    V - Left Foot Bumper Right
    B - Right Foot Bumper Left
    N - Right Foot Bumper Right

The button press status provides visual feedback for the button presses.
Multiple keys may be pressed simultaneously.

.. code-block:: bash


    ---------------------------------------  BUTTON PRESS STATUS  ---------------------------------------

    |     Chest (G)     | LFoot BumperL (C) | LFoot BumperR (V) | RFoot BumperL (B) | RFoot BumperR (N) |
    =====================================================================================================
    |      Pressed      |                   |                   |      Pressed      |                   |

.. _SimSpark's Gitlab: https://gitlab.com/robocup-sim/SimSpark/-/wikis/home