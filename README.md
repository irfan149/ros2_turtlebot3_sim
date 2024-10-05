# TurtleBot3 Simulation Workspace

This repository contains a ROS2 workspace for simulating the TurtleBot3 robot using Gazebo. The project includes the necessary URDF models, launch files, and parameter settings for simulating different models of the TurtleBot3 robot (Waffle, Waffle Pi, and Burger) and visualizing them in RViz2.

## Features
- TurtleBot3 simulation in Gazebo with ROS2.
- Pre-configured parameter files for Waffle, Waffle Pi, and Burger models.
- RViz2 visualization launch file for monitoring the robot in real-time.

## Prerequisites

Before using the repository, ensure you have the following installed:
- ROS2 (Humble/other ROS2 distribution)
- Gazebo
- RViz2
- ROS2 Navigation2 Stack
- colcon (for building ROS2 workspaces)

## Installation

1. Clone the repository:
   ```bash
   git clone <repository_url>
   cd turtlebot3_ws
   ```

2. Install dependencies (if not installed):
   ```bash
   sudo apt update
   sudo apt install ros-humble-turtlebot3-*  # or your ROS2 distro
   ```

3. Build the workspace:
   ```bash
   colcon build
   ```

4. Source the workspace:
   ```bash
   source install/setup.bash
   ```

## How to Run the Simulation

1. **Launch TurtleBot3 in Gazebo**:
   ```bash
   ros2 launch turtlebot3_fake_node turtlebot3_fake_node.launch.py
   ```

2. **View in RViz2**:
   ```bash
   ros2 launch turtlebot3_fake_node rviz2.launch.py
   ```

## File Structure

- `src/turtlebot3_fake_node/launch/`: Launch files for running the simulation (`turtlebot3_fake_node.launch.py` and `rviz2.launch.py`).
- `src/turtlebot3_fake_node/param/`: Configuration files for different TurtleBot3 models (`waffle.yaml`, `burger.yaml`, `waffle_pi.yaml`).
- `src/turtlebot3_fake_node/package.xml`: ROS2 package manifest file.

## TurtleBot3 Models Supported
- **TurtleBot3 Burger**
- **TurtleBot3 Waffle**
- **TurtleBot3 Waffle Pi**
