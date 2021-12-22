# udacity-project4
### Udacity's nano degree program: Robotics Software Engineering  
**Project Title**: Map My World?  
**Project Goals**: 
- Create 2D occupancy grid and 3D octomap from a simulated environment with the RTAB-Map package.

**Setup and pull**
```
mkdir -p $HOME/<user_workspace>/src
cd $HOME/<user_workspace>/src
git clone git@github.com:tolgakarakurt/udacity-project4.git
```
### Requirements
#### Dependencies:
- Install rtab-map [here](https://github.com/introlab/rtabmap/wiki/Installation#ubuntu)
```
$ sudo apt-get update
$ sudo apt-get install ros-kinetic-rtabmap-ros
$ sudo apt-get install libsqlite3-dev libpcl-dev libopencv-dev git cmake libproj-dev libqt5svg5-dev

```
### Build  
- Open a terminal  
- `catkin_make`

### Action
- Open a terminal
  - `roslaunch my_robot world.launch`
- Open another terminal
  - `roslaunch my_robot xxxx.launch`

**Note**: Gather [rtabmap.db here](https://drive.google.com/file/d/1JNTbnRrWtClLR8SAKnxpTy_e-f-QNBmj/view?usp=sharing)  

### Package Directory
```
TKProject4                         # Map My World Project
├── my_robot                       # my_robot package   
│   ├── config                     # map configuration files   
│   │   ├── base_local_planner_params.yaml
│   │   ├── costmap_common_params.yaml    
│   │   ├── global_costmap_params.yaml
│   │   ├── local_costmap_params.yaml              
│   ├── launch                     # launch folder for launch files   
│   │   ├── amcl.launch
│   │   ├── robot_description.launch
│   │   ├── world.launch
│   ├── maps                       # maps folder for amcl
│   │   ├── map.pgm
│   │   ├── map.yaml
│   ├── meshes                     # meshes folder for sensors
│   │   ├── hokuyo.dae
│   ├── urdf                       # urdf folder for xarco files
│   │   ├── my_robot.gazebo
│   │   ├── my_robot.xacro
│   ├── rviz                       # rviz saved configuration file
│   │   ├── default.rviz
│   ├── urdf                       # robot urdf file
│   │   ├── my_robot.gazebo
│   │   ├── my_robot.xacro
│   ├── worlds                      # world folder for world files
│   │   ├── myoffice.world
│   ├── CMakeLists.txt             # compiler instructions
│   ├── package.xml                # package info              
└──   
```