rcss3d_agent
############

rcss3d_agent Node
*****************

A ROS2 package for interacting with the rcssserver3d simulation server
used in the RoboCup 3D Simulation League.

The package aims to provide an interface that closely matches that of the
the physical Softbank NAO, rather than that of the simulation interface so
it can be used in the RoboCup Standard Platform League. The package performs
the bridging between the simulation interface and the Softbank's nao interface.

To be specific, the simulator uses different sensors and joint command formats
from a physical NAO. The conversion takes place in this package.

.. note::
    The simulation server **does not provide camera images**. This means that
    vision data, such as balls, robots, and field features are published rather
    than raw images.

.. _published-topics:
    
Published Topics
================

* **sensors/joints** (`nao_interfaces/msg/Joints`_)

* **sensors/accelerometer** (`nao_interfaces/msg/Accelerometer`_)

* **sensors/gyroscope** (`nao_interfaces/msg/Gyroscope`_)

* **sensors/angle** (`nao_interfaces/msg/Angle`_)

* **sensors/sonar** (`nao_interfaces/msg/Sonar`_)

* **sensors/fsr** (`nao_interfaces/msg/FSR`_)

* **vision/ball** (`geometry_msgs/msg/PointStamped`_)

* **vision/field_lines** (`soccer_vision_msgs/msg/FieldLineArray`_)

* **vision/goalposts** (`soccer_vision_msgs/msg/GoalpostArray`_)

* **vision/robots** (`soccer_vision_msgs/msg/RobotArray`_)

* **vision/flags** (`soccer_vision_msgs/msg/FlagArray`_)


Subscribed Topics
=================

* **effectors/joints** (`nao_interfaces/msg/Joints`_)

    Joint effector commands to be sent to the robot

Parameters
==========

* **host** (*string*, default="127.0.0.1")

    Host IP Address that simulation server is running on
    
* **port** (*int*, default=3100)

    Port number that simulation server is communicating on
    
* **team** (*string*, default="Anonymous")

    Team name of robot, to be sent to simulation server
    
* **number** (*int*, default=0)

    Player number of robot, to be sent to simulation server

* **x** (*double*, default=0.0)

    Initial position of robot along the x-axis of the field in metres, where 0.0 is the centre, and positive x is towards the opponent goal.
    
* **y** (*double*, default=0.0)

    Initial position of robot along the y-axis of the field in metres, where 0.0 is the centre, and positive y is left when facing the opponent goal.
    
* **theta** (*double*, default=0.0)

    Initial heading of robot along the x-axs of the field in radians, where 0.0 is facing the opponent goal, and positive theta is anti-clockwise.


.. _nao_interfaces/msg/Joints: https://nao-interfaces-docs.readthedocs.io/en/latest/msgs.html#joints
.. _nao_interfaces/msg/Buttons: https://nao-interfaces-docs.readthedocs.io/en/latest/msgs.html#buttons
.. _nao_interfaces/msg/Accelerometer: https://nao-interfaces-docs.readthedocs.io/en/latest/msgs.html#accelerometer
.. _nao_interfaces/msg/Gyroscope: https://nao-interfaces-docs.readthedocs.io/en/latest/msgs.html#gyroscope
.. _nao_interfaces/msg/Angle: https://nao-interfaces-docs.readthedocs.io/en/latest/msgs.html#angle
.. _nao_interfaces/msg/Sonar: https://nao-interfaces-docs.readthedocs.io/en/latest/msgs.html#sonar
.. _nao_interfaces/msg/FSR: https://nao-interfaces-docs.readthedocs.io/en/latest/msgs.html#fsr
.. _nao_interfaces/msg/Touch: https://nao-interfaces-docs.readthedocs.io/en/latest/msgs.html#touch
.. _geometry_msgs/msg/PointStamped: http://docs.ros.org/en/melodic/api/geometry_msgs/html/msg/PointStamped.html
.. _soccer_vision_msgs/msg/FieldLineArray: https://soccer-interfaces.readthedocs.io/en/latest/vision_msgs.html#fieldlinearray
.. _soccer_vision_msgs/msg/RobotArray: https://soccer-interfaces.readthedocs.io/en/latest/vision_msgs.html#robotarray
.. _soccer_vision_msgs/msg/GoalpostArray: https://soccer-interfaces.readthedocs.io/en/latest/vision_msgs.html#goalpostarray
.. _soccer_vision_msgs/msg/FlagArray: https://soccer-interfaces.readthedocs.io/en/latest/vision_msgs.html#flagarray