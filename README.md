# LiDAR

For general cloning and information, refer to this [link](https://github.com/RoboSense-LiDAR/rslidar_sdk/blob/main/README.md).

## Configuration before launch

- Go to the ```rslidar_sdk/config/config.yaml``` folder and change the ```lidar_type``` to ```RS16```.

## Launch command to view the point cloud in rviz

- Inside the ```catkin_ws``` folder, run ```catkin_make```.
- Once the build is successful, run the below commands.

```sh
source devel/setup.bash
roslaunch rslidar_sdk start.launch
```