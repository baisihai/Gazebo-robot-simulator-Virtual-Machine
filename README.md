# Gazebo-robot-simulator-Virtual-Machine

***********************************************************************************************************
<b>Ubuntu 20.04</b>
***********************************************************************************************************
User ID: ai-user<br />
Password: ai-user<br />

This is a Oracle VM VirtualBox containing the following environment:
- Oracle VM VirtualBox
- ROS noetic
- Python 3.8
- Gazebo 
- Open_manipulator gazebo model 
- Braccio gazebo model
- Intel RealSense D415 model 
- Intel RealSense D435 model 

***********************************************************************************************************
<b>Start the simulator by running each command in its own terminal.</b>
***********************************************************************************************************
<b>1) Open Manipulator Robot Simulator<br /></b>
roscore<br />
roslaunch open_manipulator_gazebo open_manipulator_gazebo.launch<br />
roslaunch open_manipulator_controller open_manipulator_controller.launch use_platform:=false<br />
<br />
In order to control the simulated OpenMANipulator-x,<br />
<p> 
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;<b>1a) start the OpenMANipulator control GUI<br /></b>
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;roslaunch open_manipulator_control_gui open_manipulator_control_gui.launch<br />
	<br />
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;OR  <br />
	<br />
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;<b>1b) keyboard remote operation<br /></b>
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;roslaunch open_manipulator_teleop open_manipulator_teleop_keyboard.launch<br />
</p>
<br />
<br />
<b>2) Braccio Robot Simulator<br /></b>
roslaunch braccio_moveit_gazebo rviz_connected_with_gz_using_moveit.launch<br />
rosrun braccio_moveit_gazebo target_object_sim.py<br />
<br />
<br />
<b>3) Intel RealSense D415<br /></b>
roslaunch realsense2_description view_d415_model_rviz_gazebo.launch<br />
<br />
<br />
<b>4) Intel RealSense D435<br /></b>
roslaunch realsense2_description view_d435_model_rviz_gazebo.launch<br />
