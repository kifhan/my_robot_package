# My Robot Intructions

## ros run sequences

on Raspberry Pi:
```
roslaunch cyglidar_d1 cyglidar.launch
roslaunch bosch_imu_driver imu.launch
```
on PC(or laptop):
```
rviz
```

## Troble shooting

Error on Ubuntu @ Raspberry Pi 4:

By not providing "FindPCL.cmake" in CMAKE_MODULE_PATH this project has
asked CMake to find a package configuration file provided by "PCL", but
CMake did not find one.

[ROS Melodic dependence record](https://www.programmersought.com/article/99652524782/)

solution:

```
sudo apt install ros-melodic-tf ros-melodic-pcl-ros libusb-1.0-0-dev -y
```

### find USB

to find usb connection info:
```
dmesg | grep ttyUSB
```
also:
```
lsusb
find /sys/bus/usb/devices/usb*/ -name dev
usb-devices
```

<br>
<br>

---
## Todo

- [ ] make imu bno055 udev rules
- [ ] cartographer
- [ ] octomap
- [ ] ssl_slam2
- [ ] set urdf
- [ ] set lcd screen
- [ ] set motor driver
- [ ] set servo driver

### In Progress

- [ ] set imu mpu6050 - may not work on raspberry pi 4b

### Done ✓

- [x] set imu bno055 - bosch-imu-driver
- [x] set CygLidar_d1
