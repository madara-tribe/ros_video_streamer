# Usb camera video stream by ROS

# ENV
## Host OS
- Mac OS
- ROS noetic

## Guset OS
- Jetson Nano
- ROS melodic
- 

# How to use

```zsh
$ git clone https://github.com/madara-tribe/ros_video_streamer.git
cd ~/catkin_make
# run usb camera
roscore
cd ~/ros_video_streamer/roscam_capture
cd roslaunch roscam_capture usb_cam.launch 

# display host PC browser
$ cd ~/ros_video_streamer/roscam_capture
$ rosrun ros_video_stream ros_video_stream _port:=10000
```

```zsh
# access address
topic_name = /usb_cam/image_raw
http://{device_ip_adress}:10000/stream?topic={topic_name}

# check ip address
$ ifconfig
```


# stracture

<img width="877" alt="stracture" src="https://user-images.githubusercontent.com/48679574/169679351-5f35c403-5bf6-4518-b603-2dc9b5b3a017.png">


# References
- [Opencv-CookBook](http://opencv.jp/cookbook/opencv_io.html)
- [mjpeg_server](https://github.com/RobotWebTools/mjpeg_server)
- [Raspberry Piロボットに搭載されたカメラの映像を遠隔PCに配信する](https://meltingrabbit.com/blog/article/2018122601/)
