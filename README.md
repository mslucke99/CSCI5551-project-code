# turtlebot_slaman

This is a ROS kinetic package that works with the Turtlebot3 burger. It allows for navigation in a dynamic, unfamiliar environment. It combines turtlebot_slam and turtlebot_navigation, hence the name: simultaneous localization and mapping and navigation. It depends on all of the other turtlebot packages to function.

### Installation

Begin by following the setup instructions found at  http://emanual.robotis.com/docs/en/platform/turtlebot3/overview/. Before compiling the catkin workspace, place the code in a directory called `turtlebot_slaman` in the workspace at the same level as the other turtlebot packages, such as `turtlebot_navigation` and `turtlebot_slam`. When compiling, make sure python 2 is used by running

```
catkin_make -DPYTHON_VERSION=2.7
```

### Usage

Make sure your remote machine and the Raspberry Pi are on the same network, that the networking configuration is set up properly as per the manual, and that you can ssh into the Raspberry Pi. Then run the following:

```
# Remote computer
roscore
```
```
# Raspberry Pi via SSH
roslaunch turtlebot3_bringup turtlebot3_robot.launch
```
```
# Remote computer
roslaunch turtlebot3_slaman turtlebot3_slaman.launch
```


### Troubleshooting

If you get errors in Rviz about no transform existing between map and the other frames, run the following command on both machines to sync the time:

```
ntpdate ntp.ubuntu.com
```
