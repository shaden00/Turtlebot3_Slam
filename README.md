#first


in this task we will see how to use Turtlebot3 with SLAM approach to create and save a map


let me first explain the setting environment 
* install ubuntu 20.04 in order to install ros1 noetic version 
*  install the gazebo11 
* for more detailed installation instructions refer to the setup section [HERE](https://emanual.robotis.com/docs/en/platform/turtlebot3/quick-start/)

**if this installations are completed we will move on to the next step**

* ubuntu 
* ros
* gazebo


#second


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

with out these packages you'll get an error while building the turtule 3 package
