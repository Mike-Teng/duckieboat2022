# duckieboat2022

## autoBox 
a = 幾號autoBNox  
ssh arg@192.168.0.a0  
repo : duckiepond-nctu  

rpi_run.sh  

set_ros_mater.sh 192.168.0.x  
set_ros_ip.sh 192.168.0.x  

source environment.sh  

### rpi : 開blueRobotic

開rosserial joy_stick  

(set_usb_port.sh for usb port udev rules)  

catkin_ws/src/duckiepond/launch/joystick_vr.launch veh:=boat  
(會開duckieboat_ros/joystick_control/src/joy_node_vr.py )  

### nano : 開roboteq  
a = 幾號autoBNox   
ssh arg@192.168.0.a3   
repo : duckiepond-nctu   

nano_run.sh  

set_ros_mater.sh 192.168.0.x  
set_ros_ip.sh 192.168.0.x  

source environment.sh  

roscd roboteq_controller   
rosrun roboteq_controller hdc2460_control_vr.py  
hdc2460_control_vr.py 要看 "/dev/ttyACM1"   
