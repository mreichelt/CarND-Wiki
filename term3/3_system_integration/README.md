# Term 3 Project 3: System Integration

Project URL: https://github.com/udacity/CarND-Capstone

In this project you will write a Robot Operating System (ROS) that will first steer a virtual car in the simulator,
and later on your code will be run on an actual car named Carla provided by Udacity.

## Known issues & typical problems

- ROS only works on Linux. You will need to install Ubuntu 16.04 if you want a native installation, or use the provided Docker file to run a preconfigured ROS installation on Ubuntu 16.04 inside a virtual machine on your Mac or Windows host.
- Performance really is key here. You can get a long way using the Docker image, but to really test your project on the simulator you will need a fast machine and probably a NVIDIA GPU for the traffic light recognition.
- If your ROS does not connect with the simulator try restarting ROS or the simulator. The setup is a little bit flaky.

## rosbag debugging

When your project submission fails the review feedback alone usually is not enough to find out what went wrong.
However, Udacity will give you a [bag file](http://wiki.ros.org/Bags) that contains all topics data - including logs,
steering messages, raw image data, LIDAR data etc. Let's see how we can get useful info out of it!

### Extract topics as CSV files

```bash
# list all topics in a bagfile
rostopic list -b bagfile.bag

# extract topic 'roslog' into a file `roslog.csv'
rostopic echo -b bagfile.bag -p /roslog > roslog.csv

# extract all topics into multiple CSV files (takes a long time)
for topic in `rostopic list -b bagfile.bag`; do rostopic echo -p -b bagfile.bag $topic > bagfile-${topic//\//_}.csv; done
```

More info on [answers.ros.org](https://answers.ros.org/question/9102/how-to-extract-data-from-bag/).

### Get all images (and video)

**TODO**

### Visualize the rosbag

**TODO**

### Replay rosbag with *rviz*  
*ROS* comes with *rviz*, a tool to display the recorded video and LiDAR data.  

#### Manual start
To manually start it you have to launch the `ros core` first, for example with `roslaunch launch/site_test.launch`.  
*You should execute the command in a __different__ terminal.*

```bash
# start rviz without configuration file
rosrun rviz rviz

# start rviz with Udacity's configuration
rosrun rviz rviz -d launch/udacity.rviz

# start rviz with video and lidar only configuration
rosrun rviz rviz -d launch/video_lidar_only.rviz
```

Configuration Files:  
- [udacity.rviz](assets/udacity.rviz)  
- [video_lidar_only.rviz](assets/video_lidar_only.rviz)

#### Automatic start
Aside from manually run *rviz* each time, you can implement it in your launch files.
Just add the following line to a suitable launch file, for example `site_test.launch`.
Preferable somewhere at the beginning to have it up and running before *ROS* is completely started.

```xml
<!-- rviz node with video and lidar only config -->
<node pkg="rviz" type="rviz" name="my_rviz" args="-d $(find styx)../../launch/video_lidar_only.rviz"/>
```

Example launch file: [site_test_rviz.launch](assets/site_test_rviz.launch)  
*Make sure to copy the configuration file to the correct place (`ros/launch/video_lidar_only.rviz`).*

More info on [wiki.ros.org/rviz](http://wiki.ros.org/rviz)

**TODO**


Help wanted - add your knowledge, tips & tricks by editing this file! 🎉
