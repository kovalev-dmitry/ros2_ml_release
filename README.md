#ROS2 ML-X Driver Binry Releases

🐧 STEP 2 – Update base system
sudo apt update && sudo apt upgrade -y
sudo apt install -y curl wget git software-properties-common lsb-release


🤖 STEP 3 – Install ROS 2 Jazzy Desktop
sudo apt install -y ros2-apt-source
sudo apt update
sudo apt install -y \
  ros-jazzy-desktop \
  python3-colcon-common-extensions \
  ros-jazzy-rmw-cyclonedds-cpp \
  ros-jazzy-image-transport ros-jazzy-cv-bridge \
  ros-jazzy-pcl-ros ros-jazzy-pcl-conversions \
  ros-jazzy-vision-opencv libopencv-dev libpcl-dev


Quick sanity check:

ros2 run demo_nodes_cpp talker
# Ctrl+C to stop

STEP 4 – Get your precompiled driver package

Download from your GitHub Release (adjust URL):

cd ~
wget https://github.com/kovalev-dmitry/ros2_ml_release/releases/download/v0.1.0/ros2_ml_amd64.tar.gz
tar xf ros2_ml_amd64.tar.gz

🚗 STEP 5 – Run the LiDAR streaming driver

Option A – if you included a run_ros2_ml.sh helper:

cd ~
chmod +x run_ros2_ml.sh
./run_ros2_ml.sh
