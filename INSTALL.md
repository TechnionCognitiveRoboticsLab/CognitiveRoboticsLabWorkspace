### Installation instructions ###

These instructions are for Ubuntu 18.04 with ROS Melodic.

First, install the following packages

```
sudo apt-get install ros-melodic-moveit ros-melodic-kobuki-* ros-melodic-ecl-streams ros-melodic-yocs-velocity-smoother ros-melodic-joy libcppunit-dev

git clone https://github.com/toeklk/orocos-bayesian-filtering.git
cd orocos-bayesian-filtering/orocos_bfl/
./configure
make
sudo make install
cd ../
make
cd ../
```

Then, run these commands to set up the ROS workspace

```
mkdir -p ros_ws/src
cd ros_ws/src/
git clone https://github.com/karpase/CognitiveRoboticsLabWorkspace.git --recurse-submodules

cd CognitiveRoboticsLabWorkspace/turtlebot2
rm -r kobuki_desktop/kobuki_qtestsuite/
mv kobuki/kobuki_description kobuki/kobuki_bumper2pc   kobuki/kobuki_node kobuki/kobuki_keyop   kobuki/kobuki_safety_controller ./
mv yujin_ocs/yocs_cmd_vel_mux yujin_ocs/yocs_controllers .
rm -rf yujin_ocs


cd ../../..
catkin_make
```
