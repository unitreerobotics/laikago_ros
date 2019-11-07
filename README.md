# Instructions: Laikago working with ROS. 

Basic function: laikago_msgs, laikago_description

Simulation related: laikago_controller, laikago_gazebo


If you want to simulate with [Gazebo](http://gazebosim.org/), we recommend **x86 platform**. **ARM platform** is not suggested for simulation.

The test environment is: Ubuntu 16.04 + ROS Kinetic. Ubuntu 18.04 + ROS Melodic is comming soon.

## Dependencies:
[Gazebo8](http://gazebosim.org/)

## Build:
* `cd ~/path-to-catkin-workspace`  (for example, replace 'path-to-catkin-workspace' with 'catkin_ws')
* `catkin_make`
* `source ~/path-to-catkin-workspace/devel/setup.bash`

### laikago_controller:
This ros-type controller allow user control joints with position, velocity and torque.

### laikago_msgs:
ros-type message, including command and state of high-level and low-level control.
It would be better if it be compiled firstly, otherwise you may have dependency problems (such as that you can't find the header file).

### laikago_description:
including mesh, urdf and xacro files of laikago.
* `roslaunch laikago_description laikago_rviz.launch`

The robot should be spawned in Rviz.

### laikago_gazebo:
Gazebo8 is recommended. Notice that it is not compatible with other versions like Gazebo7.
Make sure unders have been installed:
```
sudo apt-get install ros-kinetic-controller-manager ros-kinetic-ros-control ros-kinetic-ros-controllers ros-kinetic-joint-state-controller ros-kinetic-effort-controllers ros-kinetic-velocity-controllers ros-kinetic-position-controllers ros-kinetic-robot-controllers ros-kinetic-robot-state-publisher ros-kinetic-gazebo8-ros ros-kinetic-gazebo8-ros-control ros-kinetic-gazebo8-ros-pkgs ros-kinetic-gazebo8-ros-dev
```
* `roslaunch laikago_gazebo normal.launch`

The robot should be lying on the ground with joints not activated.

* `rosrun laikago_gazebo laikago_servo`

The robot will stand up slowly.

* `rosrun laikago_gazebo laikago_external_force`

You can add external disturbances with this node, like a push or a kick.

