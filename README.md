# RC CAR

Traxx - Slash 4x4

## Jetson TX2

Login to Tx2 through ssh
``` shell
ssh nvidia@192.168.1.187
# for X11 session - gui
ssh -X nvidia@192.168.1.187
#followed by
$ pcmanfm &
```  
password: nvidia

Turn on fan
``` shell
$ sudo ./jetson_clocks.sh
```
## Setting up the Vehicle Electronic Speed Controller
From home directory run
``` shell
$ ./bldc-tool/BLDC_Tool
```

## Running the Lidar and VESC

``` shell
$ cd catkin_ws

# turn on the lidar
$ roslaunch rplidar_ros rplidar.launch

#turn on the VESC - change the config settings if required
$ roslaunch vesc_driver vesc_driver_node.launch

# run the reinforcement learning program to demonstrate the exp on the vehicle
$ rosrun ann main_file.py

```
