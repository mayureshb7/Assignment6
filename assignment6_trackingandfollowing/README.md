This file describes running Line Following of a Turtlebot3 Burger on Gazebo and Real world and April Tag Following by Turtlebot3 Burger in real world

	1) Line Following - Gazebo
		a) Run command: "roslaunch assignment6_trackingandfollowing turtlebot3_follow_line.launch" to successfully launch world file in gazebo simulation
		b) Run command: "rosrun assignment6_trackingandfollowing line_follower_basics.py" for execution of line following in gazebo simulation
		
		
	2) Line Following - Real World
		a) Run Roscore on the pc terminal
		b) Bring up turtlebot3 burger by using this command on turtlebot terminal: roslaunch turtlebot3_bringup turtlebot3_robot.launch
		c) Bring up raspi camera by using this command on turtlebot terminal: roslaunch turtlebot3_bringup turtlebot3_rpicamera.launch
		d) Compress the raspi camera image feedback by using this command on the PC:  rosrun image_transport republish compresed in:=camera/image raw out:=camera/image_rae
		e) run command rqt_image_view to view camera
		f) Run following command on PC terminal to execute the line following code on actual bot: rosrun assignment6_trackingandfollowing follow_line_step_hsv.py
		
	3) April Tag - Real World 
	To implement April tag following in real world, following commands should be executed on terminal:
		a) Connect/SSH into turtlebot burger3 model and on another terminal window run roscore
		b) Make sure to run Roscore on ubuntu and check if IP address in ubuntu and pi are correct to establish a successfull connection: ssh ubuntu@{IP ADDRESS OF PI)
		c) Bring-up the turtlebot by using command on pi: roslaunch turtlebot3_bringup turtlebot3_robot.launch
		d) Bring up raspi camera by using this command on turtlebot terminal: roslaunch turtlebot3_bringup turtlebot3_rpicamera.launch
		e) Compress the raspi camera image feedback by using this command on the PC:  rosrun image_transport republish compresed in:=camera/image raw out:=camera/image_rae
		f) run command rqt_image_view to view camera
		g) run command: roslaunch apriltag_ros continuous_detection.launch on PC terminal window
		h) run command: rosrun apriltag_ros apriltag_follow.py on PC terminal window
	
	Refer to videos for demonstration of above tasks from assignment6_trackingandfollowing/videos
