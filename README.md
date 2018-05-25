Modification of a few bag_tools scripts for Autoware
.
Original repository: https://github.com/srv/srv_tools

bag_tools ROS wiki: http://wiki.ros.org/bag_tools

#### change_frame_id

You can use change_frame_id.py as before (see bag_tools wiki) and all the topics will be have their frame changes to one frame:
```
rosrun autoware_bag_tools change_frame_id.py -o out.bag -i in.bag -t /camera2/image_raw /camera3/image_raw /camera4/image_raw /camera5/image_raw /camera6/image_raw -f camera_frame
```
However, you can now specify a 1-to-1 mapping of frames and topics. Below, the frame of /camera2/image_raw is changed to camera2, /camera3/image_raw is changed to camera3 and so on.
```
rosrun autoware_bag_tools change_frame_id.py -o out.bag -i in.bag -t /camera2/image_raw /camera3/image_raw /camera4/image_raw /camera5/image_raw /camera6/image_raw -f camera2 camera3 camera4 camera5 camera6
```
