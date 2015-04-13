#ros_example_robot#

This repository contains an example of configuration of a robot based on the uNav board or on the RoboController board and works with the [ros_serial_bridge](https://github.com/officinerobotiche/ros_serial_bridge).

##Example robots
On this list you can see all robots with [ros_serial_bridge](https://github.com/officinerobotiche/ros_serial_bridge) in action
* [Myzharbot](https://github.com/Myzhar/ros_myzharbot_robot)
* [4UDE](https://github.com/rbonghi/ros_dude)

##Environment setup:##
Configuration with roscore run in robot and other node running on PC
###On the remote PC###
On a terminal (Ctrl+Alt+t):
```bash
$ export ROS_HOSTNAME=ubuntu.local
$ export ROS_MASTER_URI="http://ubuntu.local:11311"
```

Verify correct change with:
```bash
$ export | grep ROS
```
Execute the control GUI:
```bash
$ roslaunch example_robot_ros gui_sensor.launch
```

On a different terminal (Ctrl+Alt+t) run the keyboard teleoperation node:
```bash
$ rosrun serial_bridge drive_bridge_node
```
###On the Robot###
On a terminal (Ctrl+Alt+t):
```bash
$ export ROS_HOSTNAME=robot.local
$ export ROS_MASTER_URI="http://ubuntu.local:11311"
```

Verify correct change with:
```bash
$ export | grep ROS
```
Execute the robot nodes:
```bash
$ roslaunch example_robot_ros robot.launch
```
