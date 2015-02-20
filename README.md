# senior_design
This repository contains code that will be used to implement an autonomous ground robot using ROS (Robotic Operating System). This robot is going to be used for my Senior Design Project.

Before starting open a terminal and use:

roscore

In order to launch the kinect test use:

	source ~/devel/setup.bash

	roslaunch freenect_launch freenect.launch

	roslaunch senior_design kinect_test.launch

In order to visualize data use:

	rosrun rviz rviz

The parameters to visualize the data are:

	display type: LaserScan

	Topic: /scan

In order to connect to the Pioneer p3-DX use the following commands:

	turn robot on

	sudo chmod a+rw -R /dev/ttyUSB0

	rosrun rosaria RosAria _port:=/dev/ttyUSB0

	rostopic pub -1 /RosAria/cmd_vel geometry_msgs/Twist '{linear:  {x: 0.1, y: 0.0, z: 0.0}, angular: {x: 0.0, y: 0.0, z: 0.0}}'

In order to test publishing:

	source ~/devel/setup.bash
	
	roslaunch robot_setup_tf robot_test.launch

TODO:
http://www.ist.tugraz.at/robotics/bin/view/Main/Poineer_mapping
- Publish odometry information using tf 
