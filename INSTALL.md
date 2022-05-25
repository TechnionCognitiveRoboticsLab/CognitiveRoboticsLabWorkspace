Installation instructions


```
source /opt/ros/melodic/setup.bash
sudo apt-get install ros-melodic-moveit ros-melodic-kobuki-* ros-melodic-ecl-streams ros-melodic-yocs-velocity-smoother

mkdir -p ros_ws/src
cd ros_ws/src/
git clone https://github.com/karpase/CognitiveRoboticsLabWorkspace.git --recurse-submodules
cd ..
catkin_make
```
