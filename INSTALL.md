Installation instructions


```
source /opt/ros/melodic/setup.bash
sudo apt-get install ros-melodic-moveit

mkdir -p ros_ws/src
cd ros_ws/src/
git clone https://github.com/karpase/CognitiveRoboticsLabWorkspace.git --recurse-submodules
cd ..
catkin_make
```
