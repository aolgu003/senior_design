# senior_design
This repository contains code that will be used to implement an autonomous ground robot using ROS (Robotic Operating System). This robot is going to be used for my Senior Design Project.

In order to launch the kinect test use:

source /devel/setup.bash

roslaunch freenect_launch freenect.launch

roslaunch senior_design kinect_test.launch

In order to visualize data use:

rosrun rviz rviz

The parameters to visualize the data are:

display type: LaserScan

Topic: /scan
