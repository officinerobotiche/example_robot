setup robot:

- In command line PC
export ROS_HOSTNAME=ubuntu.local
export ROS_MASTER_URI="http://ubuntu.local:11311"

verify correct change with:
$ export | grep ROS

Launch roslaunch robot
3) roslaunch explorer_robot gui_sensor.launch
--------------------------------------------------

- In command line ROBOT
export ROS_HOSTNAME=Explorer.local
export ROS_MASTER_URI="http://ubuntu.local:11311"

verify correct change with:
$ export | grep ROS

Launch roslaunch robot
3) roslaunch explorer_robot robot.launch
