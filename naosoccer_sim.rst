naosoccer_sim Node
##################

ROS2 package for interacting with the SimSpark simulation used in the RoboCup 3D simulation league, from a nao api.

Published Topics
****************

* **sensors/joints** (`nao_interfaces/msg/Joints`_)

* **sensors/buttons** (`nao_interfaces/msg/Buttons`_)

* **sensors/accelerometer** (`nao_interfaces/msg/Accelerometer`_)

* **sensors/gyroscope** (`nao_interfaces/msg/Gyroscope`_)

* **sensors/angle** (`nao_interfaces/msg/Angle`_)

* **sensors/sonar** (`nao_interfaces/msg/Sonar`_)

* **sensors/fsr** (`nao_interfaces/msg/FSR`_)

* **sensors/touch** (`nao_interfaces/msg/Touch`_)

* **vision/ball** (`geometry_msgs/msg/PointStamped`_) - Ball vision information with frame_id 'CameraTop_frame'


Subscribed Topics
*****************

**effectors/joints** (`nao_interfaces/msg/Joints`_)

    Joint effector commands to be sent to the robot

Parameters
**********

* **host** (*string*)

    Host IP Address that simulation server is running on
    
* **port** (*int*)

    Port number that simulation server is communicating on
    
* **team** (*string*)

    Team name of robot, to be sent to simulation server
    
* **player_number** (*int*)

    Player number of robot, to be sent to simulation server

* **initial_pose_x** (*double*)

    Initial position of robot along the x-axis of the field in metres, where 0.0 is the centre, and positive x is towards the opponent goal.
    
* **initial_pose_y** (*double*)

    Initial position of robot along the y-axis of the field in metres, where 0.0 is the centre, and positive y is left when facing the opponent goal.
    
* **initial_pose_theta** (*double*)

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