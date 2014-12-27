This repository contains an example of configuration of a robot based on the
uNav board or on the RoboController board ("serial_bridge" package).

Environment setup:
==================

- On the remore PC:

$ export ROS_HOSTNAME=ubuntu.local
$ export ROS_MASTER_URI="http://ubuntu.local:11311"

verify correct change with:
$ export | grep ROS

Execute the control GUI:
$ roslaunch example_robot_ros gui_sensor.launch

On a different terminal (Ctrl+Alt+t) run the keyboard teleoperation node:
$ rosrun serial_bridge drive_bridge_node
--------------------------------------------------

- On the Robot:
export ROS_HOSTNAME=robot.local
export ROS_MASTER_URI="http://ubuntu.local:11311"

verify correct change with:
$ export | grep ROS

Execute the robot nodes:
$ roslaunch example_robot_ros robot.launch
