# first


in this task we will see how to use Turtlebot3 with SLAM approach to create and save a map


**let me first explain the setting environment** 
* install ubuntu 20.04 in order to install ros1 noetic version 
* install the gazebo11 
* for more detailed installation instructions refer to the setup section [HERE](https://emanual.robotis.com/docs/en/platform/turtlebot3/quick-start/)

**if this installations are completed we will move on to the next step**

* ubuntu 
* ros
* gazebo


# second


install dependency packages & build


**install dependen ROS packages**
```
$ sudo apt-get install ros-noetic-joy ros-noetic-teleop-twist-joy \
  ros-noetic-teleop-twist-keyboard ros-noetic-laser-proc \
  ros-noetic-rgbd-launch ros-noetic-rosserial-arduino \
  ros-noetic-rosserial-python ros-noetic-rosserial-client \
  ros-noetic-rosserial-msgs ros-noetic-amcl ros-noetic-map-server \
  ros-noetic-move-base ros-noetic-urdf ros-noetic-xacro \
  ros-noetic-compressed-image-transport ros-noetic-rqt* ros-noetic-rviz \
  ros-noetic-gmapping ros-noetic-navigation ros-noetic-interactive-markers
 ```
 
 
 **install Turtlebot packages**
```
$ sudo apt install ros-noetic-dynamixel-sdk
$ sudo apt install ros-noetic-turtlebot3-msgs
$ sudo apt install ros-noetic-turtlebot3
```

**create the source folder under the catkin workspace**
```
$ sudo apt remove ros-noetic-dynamixel-sdk
$ sudo apt remove ros-noetic-turtlebot3-msgs
$ sudo apt remove ros-noetic-turtlebot3
$ mkdir -p ~/catkin_ws/src
$ cd ~/catkin_ws/src/
$ git clone -b noetic-devel https://github.com/ROBOTIS-GIT/DynamixelSDK.git
$ git clone -b noetic-devel https://github.com/ROBOTIS-GIT/turtlebot3_msgs.git
$ git clone -b noetic-devel https://github.com/ROBOTIS-GIT/turtlebot3.git
$ cd ~/catkin_ws && catkin_make
$ echo "source ~/catkin_ws/devel/setup.bash" >> ~/.bashrc
```

**operate Gazebo & teleop turtlebot3**


now let's operate turtle3 burger in Gazebo , you can visit the simulation section of the turtle3 from [HERE](https://emanual.robotis.com/docs/en/platform/turtlebot3/quick-start/) for more details 


