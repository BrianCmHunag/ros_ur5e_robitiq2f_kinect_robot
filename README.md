# ros_ur5e_robitiq2f_kinect_robot
A moveit! robot environment includes [UR](https://www.universal-robots.com/) robot(UR5e), [Robotiq](https://robotiq.com/) 2 fingers gripper and [kinect](https://openkinect.org/wiki/Main_Page) camera.
## How to use
1. Install UR package first. See [universal_robots](http://wiki.ros.org/action/show/universal_robots?action=show&redirect=universal_robot) for more details.
``` sh
sudo apt-get install ros-kinetic-universal-robots

cd /path/to/catkin_ws/src

# retrieve the sources (replace '$DISTRO' with the ROS version you are using)
git clone -b $DISTRO-devel https://github.com/ros-industrial/universal_robot.git
```
2. Clone this repo.
```sh
git clone https://github.com/BrianCmHunag/ros_ur5e_robitiq2f_kinect_robot.git
```
3. Build the code
```sh
cd /path/to/catkin_ws

# checking dependencies (replace '$DISTRO' with the ROS version you are using)
rosdep update
rosdep install --from-paths src --ignore-src --rosdistro $DISTRO

# building
catkin_make

# source this workspace (careful when also sourcing others)
source /path/to/catkin_ws/devel/setup.bash
```
4. Execute
```
roslaunch my_ur5e_gripper_kinect_config demo.launch
```
