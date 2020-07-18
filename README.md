# Install-tutlebot3
# Tutorial  for install Turtlebot3 package with Gazebo simulation

make sure about the ROS version, here Noetic

- Install turtulebot3 package
   - Creating Workspace on ROS

     $ mkdir -p ~/catkin_ws/src
     $ cd ~/catkin_ws/
     $ catkin_make
    
   - Authintication for install 
   
     $ source devel/setup.bash
    
   - Dependence install 
     $ cd ~/catkin_ws/src/
     $ git clone https://github.com/ROBOTIS-GIT/turtlebot3_msgs.git
     $ git clone https://github.com/ROBOTIS-GIT/turtlebot3.git
     $ cd ~/catkin_ws && catkin_make
    
    
if you faced problem about "git", install by 

    $ sudo apt install git
then complete.
    - Models of TurtleBot3 are Burger, Waffle and WaffelPi. So, you need to add one of them
       - open the bashrc file by
        $ gedit ~/.bashrc
write the follwing line at bottom of the file 
 " export TURTLEBOT3_MODEL=burger " save it and close 
       - reload again 
      $ source ~/.bashrc
      
     

- Install turtulebot3_simulation package
    $ cd ~/catkin_ws/src/
    $ git clone https://github.com/ROBOTIS-GIT/turtlebot3_simulations.git
    $ cd ~/catkin_ws && catkin_make
    
    
- Launch simulation file 
    - Gazebo simulatore
       $ roslaunch turtlebot3_gazebo turtlebot3_empty_world.launch 
       - test SLAM
          $ roslaunch turtlebot3_gazebo turtlebot3_world.launch
    - RViz simulator 
       $ roslaunch turtlebot3_fake turtlebot3_fake.launch



