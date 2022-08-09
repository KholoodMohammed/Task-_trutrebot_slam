# Task_trutrebot_slam

task 4 :

How to create a map using turtlebot3, slam, simulation

Learn how to install the turtlebot3 package inside Ubuntu 20.04,ros by using the SLAM approach to create a map by moving the robot from one place to another and using sensors to discover the location around it to draw an integrated map

# steps:


Go to the website turtlebot3 by click [Quick Start Guide](https://emanual.robotis.com/docs/en/platform/turtlebot3/quick-start/#pc-setup)


Choose the appropriate version and these are the steps of the  _noetic_ version
## Set Up
### Install ROS on Remote PC



Open the terminal and enter below commands one at a time _

       $ sudo apt update
       $ sudo apt upgrade
       $ wget https://raw.githubusercontent.com/ROBOTIS-GIT/robotis_tools/master/install_ros_noetic.sh
       $ chmod 755 ./install_ros_noetic.sh 
       $ bash ./install_ros_noetic.sh
       
       
### Install Dependent ROS Packages
       $ sudo apt-get install ros-noetic-joy ros-noetic-teleop-twist-joy \
       ros-noetic-teleop-twist-keyboard ros-noetic-laser-proc \
       ros-noetic-rgbd-launch ros-noetic-rosserial-arduino \
       ros-noetic-rosserial-python ros-noetic-rosserial-client \
       ros-noetic-rosserial-msgs ros-noetic-amcl ros-noetic-map-server \
       ros-noetic-move-base ros-noetic-urdf ros-noetic-xacro \
       ros-noetic-compressed-image-transport ros-noetic-rqt* ros-noetic-rviz \
       ros-noetic-gmapping ros-noetic-navigation ros-noetic-interactive-markers
        
**Note:** Copy the entire command above

### Install TurtleBot3 Packages

       $ sudo apt install ros-noetic-dynamixel-sdk
       $ sudo apt install ros-noetic-turtlebot3-msgs
       $ sudo apt install ros-noetic-turtlebot3
       
       
## Simulation

Go to the website turtlebot3 by click [Ros Gazebo](https://emanual.robotis.com/docs/en/platform/turtlebot3/simulation/)

### Install Simulation Package

      $ cd ~/catkin_ws/src/
      $ git clone -b noetic-devel https://github.com/ROBOTIS-GIT/turtlebot3_simulations.git
      $ cd ~/catkin_ws && catkin_make
      
**Note:** we need  'turtlebot3' and  'turtlebot3_msgs' packages as prerequisite.

### Launch Simulation World 

TurtleBot3 World

       $ export TURTLEBOT3_MODEL=waffle
       $ roslaunch turtlebot3_gazebo turtlebot3_world.launch
       
_new gazebo open_


### Operate TurtleBot3

* open new terminal

       $ export TURTLEBOT3_MODEL=waffle
       
 **Note:**There are many models that can be used, including the waffle model
 
        $ roslaunch turtlebot3_teleop turtlebot3_teleop_key.launch
       
 **Note:** to control the robot in a gazebo we use the above commands 

## Simultaneous Localization and Mapping

Go to the website turtlebot3 by click [slam](https://emanual.robotis.com/docs/en/platform/turtlebot3/slam/)

 open another terminal
 
 
 ### Run SLAM Node 
 
* open new terminal
 
      $ export TURTLEBOT3_MODEL=waffle
      $ roslaunch turtlebot3_slam turtlebot3_slam.launch slam_methods:=gmapping
      
 **Note:** to control the robot in a Rviz we use the above commands 
 
 It is **important** to choose the model of the robot before controlling it
 
 
 
 
       







  

       
