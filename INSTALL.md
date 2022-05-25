Installation instructions


```
source /opt/ros/melodic/setup.bash
sudo apt-get install ros-melodic-moveit ros-melodic-kobuki-* ros-melodic-ecl-streams ros-melodic-yocs-velocity-smoother

git clone https://github.com/toeklk/orocos-bayesian-filtering.git
cd orocos-bayesian-filtering/orocos_bfl/
./configure
make
sudo make install
cd ../
make
cd ../


mkdir -p ros_ws/src
cd ros_ws/src/
git clone https://github.com/karpase/CognitiveRoboticsLabWorkspace.git --recurse-submodules


rm -r kobuki_desktop/kobuki_qtestsuite/
mv kobuki/kobuki_description kobuki/kobuki_bumper2pc   kobuki/kobuki_node kobuki/kobuki_keyop   kobuki/kobuki_safety_controller ./
mv yujin_ocs/yocs_cmd_vel_mux yujin_ocs/yocs_controllers .
rm -rf yujin_ocs


cd ../../..
catkin_make
```
