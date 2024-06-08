# gazebo-ignition-ros (Exclusively for ROS1)
The aim of this repo is to create ros ignition simulation environment that uses sdf file and then create a bridge for several topics of ignition to ros. This repository creates a simple environment with few [ignition-fuel models](https://app.gazebosim.org/fuel/models) with husky robot mounted with RGBD and segmentation camera

# gazebo-ignition installation
Note that in this repository ROS Noetic and gazebo ignition Fortress are used in combination
1. Follow this link to install ROS Noetic [ROS Noetic installation](https://wiki.ros.org/noetic/Installation/Ubuntu)
2. Follow this link to install Gazebo Fortress [Gazebo Fortress installation](https://gazebosim.org/docs/fortress/install_ubuntu)
3. Follow this link to build [ros-bridge for Fortress](https://gazebosim.org/docs/fortress/ros_integration) else follow instruction from noetic branch of the following repository [ros-bridge](https://github.com/gazebosim/ros_gz/tree/noetic)
4. Additional details of the ros-bridge noetic can be found [here](https://github.com/gazebosim/ros_gz/tree/noetic/ros_ign_bridge)

# Create a catkin ws

```
mkdir -p ~/catkin_ws/src
cd ~/catkin_ws/
catkin build

```

# clone repository inside src directory


```
cd src
git clone https://github.com/suryapilla/gazebo-ignition-ros.git
cd ~/catkin_ws/
catkin build
source devel/setup.bash
source src/gazebo-ignition-ros/semantic_segmentation_husky/scripts/set_env_variables.sh
```
Note: It is important to source the ros path run the bash file as shown in above last command

# Run the simulation
```
roslaunch semantic_segmentation_husky seg_husky.launch
```


