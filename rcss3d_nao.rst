rcss3d_nao
##########

A ROS2 package for interacting with the rcssserver3d simulation server
used in the RoboCup 3D Simulation League.

The package aims to provide an interface that closely matches that of the
the physical Softbank NAO, rather than that of the simulation interface so
it can be used in the RoboCup Standard Platform League. The package performs
the bridging between the simulation interface and the Softbank's nao interface.

To be specific, the simulator uses different sensors and joint command formats
from a physical NAO. The conversion takes place in this package.

.. note::
    The simulation server **does not provide camera images**. This means that,
    including balls, robots, and field features, **vision data is published** .

.. _published-topics:
    
Published Topics
****************

* **sensors/joint_positions** (`nao_sensor_msgs/msg/JointPositions`_)

* **sensors/accelerometer** (`nao_sensor_msgs/msg/Accelerometer`_)

* **sensors/gyroscope** (`nao_sensor_msgs/msg/Gyroscope`_)

* **sensors/angle** (`nao_sensor_msgs/msg/Angle`_)

* **vision/ball** (`soccer_vision_msgs/msg/Ball`_)

* **vision/field_lines** (`soccer_vision_msgs/msg/FieldLineArray`_)

* **vision/goalposts** (`soccer_vision_msgs/msg/GoalpostArray`_)

* **vision/robots** (`soccer_vision_msgs/msg/RobotArray`_)

* **vision/flags** (`soccer_vision_msgs/msg/FlagArray`_)


Subscribed Topics
*****************

* **effectors/joint_positions** (`nao_command_msgs/msg/JointPositions`_)

Parameters
**********

* **rcss3d/host** (*string*, default="127.0.0.1")

    Host IP Address that simulation server is running on
    
* **rcss3d/port** (*int*, default=3100)

    Port number that simulation server is communicating on
    
* **team** (*string*, default="Anonymous")

    Team name of robot, to be sent to simulation server
    
* **unum** (*int*, default=0)

    Player number of robot, to be sent to simulation server

* **x** (*double*, default=0.0)

    Initial position of robot along the x-axis of the field in metres, where 0.0 is the centre, and positive x is towards the opponent goal.
    
* **y** (*double*, default=0.0)

    Initial position of robot along the y-axis of the field in metres, where 0.0 is the centre, and positive y is left when facing the opponent goal.
    
* **theta** (*double*, default=0.0)

    Initial heading of robot from the positive x-axis of the field in radians, where 0.0 is facing the opponent goal, and positive theta is anti-clockwise.

.. _nao_sensor_msgs/msg/JointPositions: https://nao-interfaces-docs.readthedocs.io/en/latest/sensor-msgs.html#jointpositions
.. _nao_sensor_msgs/msg/Buttons: https://nao-interfaces-docs.readthedocs.io/en/latest/sensor-msgs.html#buttons
.. _nao_sensor_msgs/msg/Accelerometer: https://nao-interfaces-docs.readthedocs.io/en/latest/sensor-msgs.html#accelerometer
.. _nao_sensor_msgs/msg/Gyroscope: https://nao-interfaces-docs.readthedocs.io/en/latest/sensor-msgs.html#gyroscope
.. _nao_sensor_msgs/msg/Angle: https://nao-interfaces-docs.readthedocs.io/en/latest/sensor-msgs.html#angle
.. _nao_sensor_msgs/msg/Touch: https://nao-interfaces-docs.readthedocs.io/en/latest/sensor-msgs.html#touch
.. _soccer_vision_msgs/msg/Ball: https://soccer-interfaces.readthedocs.io/en/latest/vision_msgs.html#ball
.. _soccer_vision_msgs/msg/FieldLineArray: https://soccer-interfaces.readthedocs.io/en/latest/vision_msgs.html#fieldlinearray
.. _soccer_vision_msgs/msg/RobotArray: https://soccer-interfaces.readthedocs.io/en/latest/vision_msgs.html#robotarray
.. _soccer_vision_msgs/msg/GoalpostArray: https://soccer-interfaces.readthedocs.io/en/latest/vision_msgs.html#goalpostarray
.. _soccer_vision_msgs/msg/FlagArray: https://soccer-interfaces.readthedocs.io/en/latest/vision_msgs.html#flagarray
.. _nao_command_msgs/msg/JointPositions: https://nao-interfaces-docs.readthedocs.io/en/latest/command-msgs.html#jointpositions