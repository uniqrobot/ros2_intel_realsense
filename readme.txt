sudo apt-key adv --keyserver keys.gnupg.net --recv-key F6E65AC044F831AC80A06380C8B3A55A6F3EFCDE || sudo apt-key adv --keyserver hkp://keyserver.ubuntu.com:80 --recv-key F6E65AC044F831AC80A06380C8B3A55A6F3EFCDE
sudo add-apt-repository "deb http://realsense-hw-public.s3.amazonaws.com/Debian/apt-repo bionic main" -u
sudo apt-get install librealsense2-dkms
sudo apt-get install librealsense2-utils
sudo apt-get install ros-foxy-cv-bridge ros-foxy-message-filters ros-foxy-image-transport
sudo apt-get install -y libssl-dev libusb-1.0-0-dev pkg-config libgtk-3-dev
sudo apt-get install -y libglfw3-dev libgl1-mesa-dev libglu1-mesa-dev
sudo apt-get install librealsense2-dev

1:查看设备编号
    rs-enumerate-devices
2:启动:
    ros2 run realsense_node realsense_node __params:=`ros2 pkg prefix realsense_examples`/share/realsense_ros/config/d435i.yaml __ns:=/d435i
或者
    ros2 launch realsense_examples rs_camera.launch.py