# Gazebo-robot-simulator-Virtual-Machine

***********************************************************************************************************
##Ubuntu 20.04
***********************************************************************************************************
User ID: ai-user<br />
Password: ai-user<br />

Environment
- Oracle VM VirtualBox
- ROS noetic
- Python 3.8
- Gazebo 
- Open_manipulator gazebo model 
- Braccio gazebo model
- Intel RealSense D415 model 
- Intel RealSense D435 model 

***********************************************************************************************************
##Start the simulator by running each command in its own terminal.
***********************************************************************************************************
<p>
###1) Open Manipulator Robot Simulator<br />
roscore<br />
roslaunch open_manipulator_gazebo open_manipulator_gazebo.launch<br />
roslaunch open_manipulator_controller open_manipulator_controller.launch use_platform:=false<br />
</p>
<p>
	
In order to control the simulated OpenMANipulator-x,<br />
	1a) start the OpenMANipulator control GUI<br />
	roslaunch open_manipulator_control_gui open_manipulator_control_gui.launch<br />
	<br />
	OR  <br />
	<br />
	1b) keyboard remote operation<br />
</p>
<p>
	roslaunch open_manipulator_teleop open_manipulator_teleop_keyboard.launch
</p>
<p>
2) Braccio Robot Simulator
</p>
<p>
roslaunch braccio_moveit_gazebo rviz_connected_with_gz_using_moveit.launch
</p>
<p>
rosrun braccio_moveit_gazebo target_object_sim.py
</p>
<p>
3) Intel RealSense D415
</p>
<p>
roslaunch realsense2_description view_d415_model_rviz_gazebo.launch
</p>
<p>
4) Intel RealSense D435
</p>
<p>
roslaunch realsense2_description view_d435_model_rviz_gazebo.launch
</p>
