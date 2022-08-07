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


**Install Simulation Package**
The TurtleBot3 Simulation Package requires turtlebot3 and turtlebot3_msgs packages as prerequisite. Without these prerequisite packages, the Simulation cannot be launched
```
$ cd ~/catkin_ws/src/
$ git clone -b noetic-devel https://github.com/ROBOTIS-GIT/turtlebot3_simulations.git
$ cd ~/catkin_ws && catkin_make
```
**set burger for turtle3 model parameter and run Gazebo** 
```
$ export TURTLEBOT3_MODEL=burger
$ roslaunch turtlebot3_gazebo turtlebot3_world.launch
```
![image](https://user-images.githubusercontent.com/97844314/183302801-e90b474f-c538-4c8f-a727-d4474a68ab5b.jpeg)


**when gazebo is executed create a new terminal and run the teleoperate**

In order to teleoperate the TurtleBot3 with the keyboard, launch the teleoperation node with below command in a new terminal window
```
$ export TURTLEBOT3_MODEL=burger
$ roslaunch turtlebot3_teleop turtlebot3_teleop_key.launch
```
![image](https://user-images.githubusercontent.com/97844314/183302997-61261a38-231f-4aa9-882b-860a89e327a7.jpeg)


# third

**SLAM & save a map**

in the next setup we will review how to create a map using slam and save the map

* run Gazebo using an identical execution command we used previously 
```
$ export TURTLEBOT3_MODEL=burger
$ roslaunch turtlebot3_teleop turtlebot3_teleop_key.launch
```

if gazebo is up and running create a new terminal and run turtle3 **slam** node
```
$ export TURTLEBOT3_MODEL=burger
$ roslaunch turtlebot3_slam turtlebot3_slam.launch
```

when turtle3 slam node is launched successfully the RViz window will be opened 

![image](https://user-images.githubusercontent.com/97844314/183304867-b3d7b6d5-6e0d-4eff-bce2-a56a721c97ce.jpeg)


