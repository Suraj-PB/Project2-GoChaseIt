# Project 2: Go Chase It

   Create a package to chase a white ball using ROS and Gazebo. Use Rviz for the visualization. 
   
# Project Structure

     .Project2-GOChaseIt                         # Go Chase It Project
    ├── my_robot                       # my_robot package                   
    │   ├── launch                     # launch folder for launch files   
    │   │   ├── robot_description.launch
    │   │   ├── world.launch
    │   ├── meshes                     # meshes folder for sensors
    │   │   ├── hokuyo.dae
    │   ├── urdf                       # urdf folder for xarco files
    │   │   ├── my_robot.gazebo
    │   │   ├── my_robot.xacro
    │   ├── world                      # world folder for world files
    │   │   ├── <yourworld>.world
    │   ├── CMakeLists.txt             # compiler instructions
    │   ├── package.xml                # package info
    ├── ball_chaser                    # ball_chaser package                   
    │   ├── launch                     # launch folder for launch files   
    │   │   ├── ball_chaser.launch
    │   ├── src                        # source folder for C++ scripts
    │   │   ├── drive_bot.cpp
    │   │   ├── process_image.cpp
    │   ├── srv                        # service folder for ROS services
    │   │   ├── DriveToTarget.srv
    │   ├── CMakeLists.txt             # compiler instructions
    │   ├── package.xml                # package info                  
    └──  
    
# Setup
  ### Prerequesites
  1. To run this package first install ROS and Gazebo on your system
      * ROS installation  (http://wiki.ros.org/Installation/Ubuntu)
      * Gazebo Installation (http://gazebosim.org/tutorials?tut=install_ubuntu)
      
  2. Compiler(gcc/g++) and Cmake
  
  ### Build and Launch Project
  1. Clonning, initialization and building of project using catkin workspace.
  
    $ mkdir catkin_ws && cd catkin_ws
    $ git clone https://github.com/Suraj-PB/Project2-GoChaseIt.git
    $ mv Project2-GoChaseIt src
    $ cd src && catkin_init_workspace
    $ cd ..
    $ catkin_make
  
  2. Launch a world file 
  
    $ source devel/setup.bash
    $ roslaunch my_robot world.launch
    
  3. Open another terminal and lauch ball chaser package
    $ source devel/setup.bash
    $ roslaunch ball_chaser ball_chaser.launch
      
  4. Move a white ball around a world and see the robot will follow the ball. Have a fun playing!

     


  
  
