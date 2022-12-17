# orange_mapping
This package provides slam functionality for the orange robot.
## Setup
```
./setup.sh
```
## LIO-SAM
- From gazebo simulation
```
roslaunch orange_mapping lio_sam_slam.launch
roslaunch tsukuba2022 start_sim.launch
rosservice call /lio_sam/save_map 1.0 "/Downloads/LOAM/"
```
- From rosbag
```
roslaunch orange_mapping lio_sam_slam.launch create_map_from_rosbag:=true
rosbag play your_bag.bag -r 1 --clock
rosservice call /lio_sam/save_map 1.0 "/Downloads/LOAM/"
```
