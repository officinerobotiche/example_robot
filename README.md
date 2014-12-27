#example_robot_ros#

This repository contains an example of configuration of a robot based on the uNav board or on the RoboController board ("serial_bridge" package).

##Environment setup:##

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
