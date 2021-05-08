nao_buttons_sim
###############

ROS2 package for simulation button presses on a NAO, through keypress events.

Publishes at 50Hz. (This may change)

Published Topics
****************

* **buttons** (`nao_interfaces/msg/Buttons`_)

Parameters
**********

* **frequency** (*int*, default=50)

    Frequency of publishing on the buttons topic in Hz.

Example
*******

::

    ros2 run nao_buttons_sim nao_buttons_sim

.. _nao_interfaces/msg/Buttons: https://nao-interfaces-docs.readthedocs.io/en/latest/msgs.html#buttons