joints_to_joint_state Node
##########################

ROS2 package for converting nao_interfaces/msg/Joints.msg to sensor_msgs/msg/JointState.msg.
This node is required mainly for visualization in RViz.

Published Topics
****************

* **joint_states** (*sensor_msgs/msg/JointState*)

Subscribed Topics
*****************

* **sensors/joints** (*nao_interfaces/msg/Joints*)
