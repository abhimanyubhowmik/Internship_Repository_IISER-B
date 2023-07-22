<h1 align="center">Object Detectation and Tracking using Turtle Bot</h1>

<p align="center">
<img src="Images/moonlab.png" width="1500" height="">
</p>


> **Abstract:** *Autonomous rovers are mobile robots, designed to operate in various conditions without any human intervention. These rovers are equipped with sensors, actuators, and control systems that enable them to navigate and interact with their environment. They are widely employed in fields like exploration, search and rescue, environmental monitoring, and surveillance. This research presents the construction and development of an autonomous rover that integrates parallel object tracking, videography, and collision avoidance. The proposed system is designed to operate in real-world scenarios where the rover can navigate safely and capture high-quality visual data of its targeted moving object which can be a living or non-living thing. The rover's control system is based on a combination of classical controllers such as PID controller accompanied by computer vision techniques, enabling it to detect and track objects at a parallel level in its environment, avoid obstacles and collisions, and record video footage with minimal hardware requirements. The proposed system's performance will be evaluated through extensive testing, where the rover's ability to navigate complex environments and capture high-quality visual data will be assessed.*

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




<h2>ROS Nodes</h2>

<img src="Images/rqt_plot.png" alt="wolfram" width=""/>

<h2>Results</h2>

<h3>1. Simulation</h3>


https://github.com/abhimanyubhowmik/TrackerBot/assets/72135456/eaed8dc8-102f-4198-b432-6f4fb06c4e33


<p align="center">

<table border="0">
 <tr>
    <td><img src="Images/Pos_and_Vel.png" alt="turtlebot-side 1" width="250"/></td>
    <td><img src="Images/Covariance%20Matrices.png" alt="turtlebot-side 2" width="250"/></td>
 </tr>
</table>

<h3>2. Hardware Implementation</h3>


 <tr>
    <td><img src="Images/rqt.png" alt="turtlebot-side 1" width="250"/></td>
    <td><img src="Images/kalman_filter.png" alt="turtlebot-side 2" width="250"/></td>
 </tr>


  

## Contributors:

[Abhimanyu Bhowmik](https://github.com/abhimanyubhowmik), 
[Madhushree Sannigrahi](https://github.com/Madhushree2000)



## Links:

[MoonLab@IISER-B](https://moonlab.iiserb.ac.in/)

[Dr. P.B. Sujit](https://scholar.google.com/citations?user=qqwyAwoAAAAJ&hl=en)


