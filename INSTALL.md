Installation instructions

```
source /opt/ros/melodic/setup.bash
mkdir -p ros_ws/src
cd ros_ws/src/
git clone https://github.com/karpase/CognitiveRoboticsLabWorkspace.git --recurse-submodules
cd ..
rosdep install --from-paths src --ignore-src
catkin_make
```
