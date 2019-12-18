This is a ros package that works with the turtlebot3 burger.
It allows navigation in an unfamiliar environment
It relies on the lidar sensor, which is not very good on the turtlebot
we called this slaman because it is SLAM and it also uses the navigation
stack, so SLAM And Navigation = SLAMAN. Don't worry, we also cringe
when we hear that name. The name Salmon Autonomous Localization+Mapping
On Navigation would have been better because then it would be a
recursive acronym and a fish name allowing more cringing. But not as
much as the fact that this file was written directly in github,
intentionally, exclusively for the purpose of being cringeworthy.

########################################################################
Installation
########################################################################

in order to install this, first, download it, then put it in a catkin
workspace, in a package called turtlebot3_slaman. Refer to the ROS 
documentation for more information on catkin workspaces. When building,
use the command on the following line:
catkin_make -DPYTHON_VERSION=2.7
The above command is unnecessary if the default python version on your
system is python 2, but at this point, python 2 is about to lose support
so that commmand is probably necessary.

########################################################################
Usage
########################################################################

When using this launch file, first, make sure that the instructions
found on http://emanual.robotis.com/docs/en/platform/turtlebot3/overview/
for setup are followed. Make sure to set up your .bashrc file so that
the ip addresses are correct. If the wrong ip address is used, then
this will not work. Make sure that is also done on the pi, and that
they are on the same network. All of this was mentioned in the manual
above. Next, run roscore on the remote PC. Wait for it to finish starting
up. Then, run the command on the following line on the turtlebot:
roslaunch turtlebot3_bringup turtlebot3_robot.launch
Then, on the remote PC, run
roslaunch turtlebot3_slaman turtlebot3_slaman.launch
If the package you placed these files in had a different name, replace the
first "turtlebot3_slaman with whatever the package name was and try
running that command again.
