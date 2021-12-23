# Visual-servoing
Application of frame transformations and differential drive kinematics to implement a simple visual servoing behavior on the Turtlebot3.
AprilTags are simple 2D barcodes (similar to QR codes) that are often used as visual fiducials
in robotics applications. Because the corners of these tags are easy to detect in images, and the
tags themselves have a known geometry, it is possible to estimate their pose relative to a calibrated camera from a single image.
The goal is to drive a Turtlebot3 to a target pose that is specified with respect to an AprilTag – this is the same basic behavior that industrial and household robots (e.g. Roombas) use when “auto-docking” themselves to a base station. Here the bot has to detect the april tag, run a transformation from april tag frame to bot base frame and stop at 0.12m from the tag. The simplest form of visual servoing.

Terminal 1: roscore
Terminal 2: roslaunch turtlebot3_mr apriltag_gazebo.launch
Terminal 3: rosrun rviz rviz -d config/rviz.rviz
Terminal 4: python3 final.py 
