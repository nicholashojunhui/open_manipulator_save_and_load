## Description 
This is a open manipulator ROS application package. Disable torque of Open manipulator and move Open manipulator by hand. Then,the joint value is saved in the file at 0.1 msec intervals.Then you can read the file and move open manipulator at ROS.  

Click image to link to YouTube video.  
[![Video Label](http://img.youtube.com/vi/PH-7JwGH9uM/0.jpg)](https://youtu.be/PH-7JwGH9uM?t=0s)   


## Setting  
0 step. open manipulator Ros packages setting (done).   

1 step. open_manipulator_save_and_load package setting.   
- Navigate to catkin_ws --> src folder
- copy and paste "open_manipulator_save_and_load" file in the src folder
- In the command terminal, type:
$ ~/catkin_ws && catkin_make 

## RUN  
$ roslaunch open_manipulator_gazebo open_manipulator_gazebo.launch
$ roslaunch open_manipulator_controller open_manipulator_controller.launch use_platform:=false
$ roslaunch open_manipulator_save_and_load save_and_load.launch
```
You can select the below menu by the keyboard input.  
```bash
---------------------------
1. Start to save joint data
2. Stop to save joint data
3. Load to joint data
---------------------------
```
0 step.   
Enter 1 by keyboard, The torque of open manipulator will be disabled, So you can move open manipulator by hand.  
1 step.   
Enter 2 by keyboard, So the movement of open manipulator will be saved as a file in the cfg folder.  
2 step.   
Enter 3 by keyboard, Then Open manipulator will move itself by loading the file.  

## Speed Tunning
When loading the movement file by pressing the 3 key, you can modify the speed of the movement by increasing the number below.  
file location is nodes/save_and_load  
```bash
                self.count = self.count + 15
                #self.count = self.count + 8 # movement speed slow
                #self.count = self.count + 25  # movement speed fast
```

  
