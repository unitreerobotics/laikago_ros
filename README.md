# laikago_ros
Laikago working with ROS. The test environment is: Ubuntu 16.04 + ROS Kinetic.

## laikago_rviz: Unitree Laikago Rviz Visualization

We use Xacro formatted description, which is simpler and cleaner than URDF format.
### Instructions:
#### Build:
* `cd ~/path-to-catkin-workspace`
* `catkin_make`
#### Run:
* `cd ~/path-to-catkin-workspace/src/laikago_rviz/launch`
* `roslaunch ./rviz.launch`

Or you can just run:
* `roslaunch laikago_rviz rviz.launch`
The robot should be spawned in Rviz.
