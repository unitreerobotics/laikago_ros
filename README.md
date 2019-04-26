# laikago_ros
Laikago working with ROS. The test environment is: Ubuntu 16.04 + ROS Kinetic.

## laikago_rviz: Unitree Laikago Rviz Visualization

We use Xacro formatted description, which is simpler and cleaner than URDF format.
### Instructions:
#### Build:
* `cd ~/path-to-catkin-workspace` (for example, replace 'path-to-catkin-workspace' with 'catkin_ws')
* `catkin_make`
* `source ~/path-to-catkin-workspace/devel/setup.bash`
#### Run:
* `roslaunch laikago_rviz rviz.launch`

The robot should be spawned in Rviz.
