# LiDAR

For general cloning and information, refer to this [link](https://github.com/RoboSense-LiDAR/rslidar_sdk/blob/main/README.md). Please note that you do not have to follow any steps mentioned there. It is just for your reference and understanding. You can follow the steps mentioned here.

## Configuration before launch

- Open the *CMakeLists.txt* in the project，modify the line  on top of the file **set(COMPILE_METHOD ORIGINAL)** to **set(COMPILE_METHOD CATKIN)**.

```cmake
#=======================================
# Compile setup (ORIGINAL,CATKIN,COLCON)
#=======================================
set(COMPILE_METHOD CATKIN)
```

- Copy the file *package_ros1.xml*  in the rslidar_sdk to *package.xml*

- Create a new workspace folder, and create a *src* folder in it with the following command.

```sh
mkdir -p catkin_ws/src
```

- Then clone the *rslidar_sdk* project into the *src* folder with the following command.

```sh
git clone https://github.com/RoboSense-LiDAR/rslidar_sdk.git
```

- Next step, run the following commands.

```sh
cd rslidar_sdk
git submodule init
git submodule update
```

- Go to the ```rslidar_sdk/config/config.yaml``` file and change the ```lidar_type``` to ```RS16```.

## Launch command to view the point cloud in rviz

- Inside the ```catkin_ws``` folder, run ```catkin_make```.
- Once the build is successful, run the below commands.

```sh
source devel/setup.bash
roslaunch rslidar_sdk start.launch
```