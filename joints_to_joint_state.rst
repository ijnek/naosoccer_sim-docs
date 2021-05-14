joints_to_joint_state
#####################

ROS2 package for converting `nao_interfaces/msg/Joints`_ to `sensor_msgs/msg/JointState`_.
This node is required mainly for visualization in RViz.

Published Topics
****************

* **joint_states** (`sensor_msgs/msg/JointState`_)

Subscribed Topics
*****************

* **sensors/joints** (`nao_interfaces/msg/Joints`_)


.. _sensor_msgs/msg/JointState: http://docs.ros.org/en/melodic/api/sensor_msgs/html/msg/JointState.html
.. _nao_interfaces/msg/Joints: https://nao-interfaces-docs.readthedocs.io/en/latest/msgs.html#joints