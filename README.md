# My Robot — Mobile Base + 2-DOF Arm (ROS 2)

A small ROS 2 project: a differential-drive mobile base with a 2-DOF robotic arm and a camera.  
Simulated in `ros_gz_sim` (gz-sim) and visualized with RViz. Includes bridge configuration so ROS ↔ Gazebo topics work.

---

## Quick Start

```bash
# 1) Put the repo into a workspace
mkdir -p ~/ros2_ws/src
cd ~/ros2_ws/src
git clone https://github.com/YOUR_USERNAME/REPO_NAME.git

# 2) Build
cd ~/ros2_ws
colcon build

# 3) Source
source /opt/ros/jazzy/setup.bash    # (or your ROS 2 distro)
source ~/ros2_ws/install/setup.bash

# 4) Run simulation + RViz (bringup)
ros2 launch my_robot_bringup my_robot_gazebo.launch.xml
# (or to just view the robot_description in RViz)
ros2 launch my_robot_description display.launch.xml
