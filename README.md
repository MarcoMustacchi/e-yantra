<p align="center">
  <img src="https://github.com/MarcoMustacchi/e-yantra/blob/main/VitaranaDrone.jpg" width="1440">
</p>

## Goal 
Deploy a drone in a simulator that delivers and returns packages in a cityscape while implementing concepts in control systems, image processing, path planning and scheduling.

## Setup 
Ubuntu 18.04 with ROS Melodic using [Terminator](https://gnome-terminator.org/) as shell

## Installation
###### Create a ROS workspace

```
mkdir -p ~/<WORKSPACE_NAME>/src
cd ~/<WORKSPACE_NAME>/src
catkin_init_workspace
```

###### Setting up ROS packages from Git
```
cd ~/<WORKSPACE_NAME>/src

git clone https://github.com/smitkesaria/vitarana_drone.git
git clone https://github.com/smitkesaria/additional_package_for_vd.git
git clone https://github.com/simmubhangu/pid_tune.git

```

###### Additional to do (make content in the parent directory and rename)

```
cd additional_package_for_vd/
mv gazebo_ros_link_attacher/* .
rmdir gazebo_ros_link_attacher/
mv additional_package_for_vd/ gazebo_ros_link_attacher
```

###### Build the Packages

```
cd ~/<WORKSPACE_NAME>/
catkin_make 
```

## Preliminary Step
Remember to add 
```
source /opt/ros/melodic/setup.bash
source ~/<WORKSPACE_NAME>/devel/setup.bash
```
at the end of your **.bashrc** file

