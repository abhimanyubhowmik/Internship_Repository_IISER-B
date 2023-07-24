<h1 align="center">Object Detectation and Tracking using Turtle Bot</h1>

<p align="center">
<img src="Images/moonlab.png" width="1500" height="">
</p>


> **About:** *During a 6-month hybrid internship at IISER Bhopal MoonLab, under the guidance of Professor P. B. Sujit, we successfully created an object tracking Rover. The internship consisted of 2 months of offline work followed by 4 months of online collaboration. The Rover is equipped with YOLO V3 for detecting objects in video stream data, and we employed the Kalman Filter to process this data. The filtered output was then used as input for a custom PID controller, which we fine-tuned based on the camera's positional error and the estimated velocity of the moving object. To validate the system, we conducted tests using Webots simulation and Turtlebot 3 Burger, and the results have been generated.*

<h2>TurtleBot 3 : Burger</h2>

<p align="center">

<table border="0">
 <tr>
    <td><img src="Images/Side%201.jpg" alt="turtlebot-side 1" width="250"/></td>
    <td><img src="Images/Side%202.jpg" alt="turtlebot-side 2" width="250"/></td>
 </tr>
</table>



</p>


<h3>LoginID & Password</h3>  

```
moonlab
iiserb@1234
```

<h2>ROS Execution Commands</h2>

<h4>1. Vision</h4>

```roslaunch drive_rover vision.launch```

<h4>2. Drive</h4>  

```roslaunch drive_rover drive.launch```

<h4>3. Bringup</h4>

```
source ros/turtlebot/devel/setup.bash

export OPENCR_MODEL=burger

export OPENCR_PORT=/dev/ttyACM0

sudo chmod a+rw /dev/ttyACM0

cd ros/opencr_update/

./update.sh $OPENCR_PORT $OPENCR_MODEL.opencr

roslaunch turtlebot3_bringup turtlebot3_robot.launch 
```

<h4>4. Teleop</h4>

```
source ros/turtlebot/devel/setup.bash

roslaunch turtlebot3_teleop turtlebot3_teleop_key.launch
```

<h4>5. SLAM</h4>

```
source ros/turtlebot/devel/setup.bash

export TURTLEBOT3_MODEL=burger

export LDS_MODEL=LDS-01

roslaunch turtlebot3_slam turtlebot3_slam.launch
```



<h2>Results</h2>

<h3>1. Simulation</h3>




https://github.com/abhimanyubhowmik/Internship_Repository_IISER-B/assets/72135456/bab570ba-ea04-4512-a105-00b954f58124




<p align="center">

<table border="0">
 <tr>
    <td><img src="Images/Pos_and_Vel.png" alt="turtlebot-side 1" width="500"/></td>
    <td><img src="Images/Covariance%20Matrices.png" alt="turtlebot-side 2" width="500"/></td>
 </tr>
</table>

<h3>2. Hardware Implementation</h3>


https://github.com/abhimanyubhowmik/Internship_Repository_IISER-B/assets/72135456/1c30e134-39f1-46ca-a35c-0f4f1d5c10f9



https://github.com/abhimanyubhowmik/Internship_Repository_IISER-B/assets/72135456/f36e2b71-f36c-4d6f-abe0-5d2f44dade5f




<p align="center">

<table border="0">
 <tr>
    <td><img src="Images/rqt.png" alt="turtlebot-side 1" width=""/></td>
    <td><img src="Images/kalman_filter.png" alt="turtlebot-side 2" width=""/></td>
 </tr>

</table>
  

## Collaborators:

[Abhimanyu Bhowmik](https://github.com/abhimanyubhowmik), 
[Madhushree Sannigrahi](https://github.com/Madhushree2000),
[Dr. P.B. Sujit](https://scholar.google.com/citations?user=qqwyAwoAAAAJ&hl=en)



## Links:

[MoonLab@IISER-B](https://moonlab.iiserb.ac.in/)



