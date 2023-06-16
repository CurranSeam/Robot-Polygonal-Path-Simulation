# Robot-polygonal-path-simulation
A ROS/Gazebo simulation for a robot traversal of any polygonal path using two geometric parameters. (number of sides of the polygon and the length of the sides).

# Instructions
The following steps assume that you already have a catkin workspace, a created package, and the necessary dependencies.

In robot_polygon_path.launch edit the following line:
- `<node pkg="<YOUR_PACKAGE>" type="robot_polygon_path" name="robot_polygon_path" output="screen">`
- replace <YOUR_PACKAGE> with the package that you have built

How to run simulation:
- Open an Ubuntu terminal
- Run `cd catkin_ws/`
- Run `source devel/setup.bash`
- Run `roslaunch <YOUR_PACKAGE> gazebo_navigation_rviz.launch`
- Go to Rviz and set 2d pose estimate to current robot location in gazebo
- Open another Ubuntu terminal
- Run `cd catkin_ws/`
- Run `source devel/setup.bash`
- Run `roslaunch <YOUR_PACKAGE> robot_polygon_path.launch`

If you want to change rosparams to make different polygon paths:
- Change robot_polygon_path.launch file variables
- Run catkin_make
- Run devel/setup.bash
