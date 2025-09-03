# ros2-sim-vslam

- download checkboard, default.sdf
- overwrite default.sdf in world of px4_gz500, edit the path to your location of your checkboard

## Update
- ros_gz : https://github.com/gazebosim/ros_gz/tree/humble

### Commands
```
PX4-Autopilot$ make px4_sitl gz_x500_vision
ros2 launch mavros px4.launch fcu_url:="udp://:14540@127.0.0.1:14557"
```

### Camera Calibration
```
make px4_sitl gz_x500_vision
ros2 run ros_gz_image image_bridge /camera/image_raw
ros2 run camera_calibration cameracalibrator --size 6x6 --square 0.02 --ros-args -r image:=/camera/image_raw -p camera:=/camera
```

## Recommended File structure

https://github.com/Jaeyoung-Lim/px4-offboard

Dependency:
mavros
