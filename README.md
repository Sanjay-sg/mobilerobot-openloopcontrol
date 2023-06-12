# MobileRobot-Openloopcontrol
## Aim:

To develop a python control code to move the mobilerobot along the predefined path.

## Equipments Required:
1. RoboMaster EP core
2. Python 3.7

## Procedure
```
## Step1:
Initiate the MobileRobot.
## Step2:
Connect your PC with the MobileRobot.
## Step3:
Program the movements of the robot using python code
## Step4:
Execute the python program.
```
## Program
```
from robomaster import robot
import time
from robomaster import camera

if __name__ == '__main__':
    ep_robot = robot.Robot()
    ep_robot.initialize(conn_type="ap")

    ep_chassis = ep_robot.chassis
    ep_led = ep_robot.led
    ep_camera = ep_robot.camera

    print("Video streaming started.....")
    ep_camera.start_video_stream(display=True, resolution = camera.STREAM_360P)

    '''
    x = x-axis movement distance,( meters) [-5,5]
    y = y-axis movement distance,( meters) [-5,5]
    z = rotation about z axis ( degree)[-180,180]
    xy_speed = xy axis movement speed,( unit meter/second) [0.5,2]
    '''
    ep_chassis.move(x=3, y=0, z=0, xy_speed=1).wait_for_completed()
    ep_led.set_led(comp = "all",r=0,g=255,b=0,effect="on")

    ep_chassis.move(x=0, y=0, z=80, xy_speed=1).wait_for_completed()
    ep_led.set_led(comp = "all",r=0,g=0,b=255,effect="on")

    ep_chassis.move(x=0.9, y=0, z=0, xy_speed=1).wait_for_completed()
    ep_led.set_led(comp = "all",r=0,g=255,b=255,effect="on")

    ep_chassis.move(x=0, y=0, z=87, xy_speed=1).wait_for_completed()
    ep_led.set_led(comp = "all",r= 0 , g=128,b=128,effect="on")

    ep_chassis.move(x=1.5, y=0, z=0, xy_speed=1).wait_for_completed()
    ep_led.set_led(comp = "all",r= 255 , g=255,b=0,effect="on")

    ep_led.set_led(comp = "all",r= 0 , g=255,b=255,effect="on")

    ep_chassis.move(x=0, y=0 ,z=-27,xy_speed=1).wait_for_completed()
    ep_led.set_led(comp = "all",r=192, g=192,b=192,effect="on")

    ep_chassis.move(x=1.2, y=0 ,z=0,xy_speed=1).wait_for_completed()
    ep_led.set_led(comp = "all",r=102, g=0,b=102,effect="on")

    ep_chassis.move(x=0.5, y=0 ,z=45,xy_speed=1).wait_for_completed()
    ep_led.set_led(comp = "all",r=255, g=255,b=255,effect="on")

    ep_chassis.move(x=1.3,y=0,z=0,xy_speed=1).wait_for_completed()
    ep_led.set_led(comp = "all",r=150, g=150 , b =150,effect ="on")

    ep_led.set_led(comp = "all",r=255, g=128,b=128,effect="on")

    ep_chassis.move(x=0,y=0,z=88,xy_speed=1).wait_for_completed()
    ep_led.set_led(comp = "all",r=102, g=102 , b = 153,effect ="on")

    ep_chassis.move(x=2.1,y=-0,z=0,xy_speed=1).wait_for_completed()
    ep_led.set_led(comp = "all",r=0, g=51 , b =0,effect ="on")

    ep_chassis.move(x=0,y=-0,z=85,xy_speed=1).wait_for_completed()
    ep_led.set_led(comp = "all",r=51, g=153 , b =102,effect ="on")

    ep_chassis.move(x=0.6,y=-0,z=0,xy_speed=1).wait_for_completed()
    ep_led.set_led(comp = "all",r=255, g=153 , b =204,effect ="on")

    ep_chassis.move(x=0,y=-0,z=360,xy_speed=1).wait_for_completed()
    ep_led.set_led(comp = "all",r=204, g=153 , b =255,effect ="on")
    ep_led.set_led(comp = "all",r=153, g=204 , b =0,effect ="on")
    time.sleep(4)


    ep_camera.stop_video_stream()
    print("Stopped video streaming.....")
    ep_robot.close()


    
    ep_robot.close()
```

## MobileRobot Movement Image:

![image](https://github.com/Sanjay-sg/mobilerobot-openloopcontrol/assets/119559022/1e474312-6f7e-4670-89f5-48b2c1d7b455)


## MobileRobot Movement Video:

https://www.youtube.com/shorts/67t4sYK1G1s

## Result:
Thus the python program code is developed to move the mobilerobot in the predefined path.


<br/>
<br/>

```
Mobile Robotics Laboratory
Department of Artificial Intelligence and Data Science/ Machine Learning
Saveetha Engineering College
```
