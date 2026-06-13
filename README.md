# Ground Robot Navigation with EKF Localization

Webots simulation of an e-puck robot performing autonomous navigation in a maze-like environment with noisy sensors.

## Overview
Implemented a navigation system for an e-puck ground robot to reach a goal while handling noisy odometry and sensor data. Used an **Extended Kalman Filter (EKF)** to fuse landmark observations (from camera) with odometry for accurate localization, preventing error accumulation that would send the robot off course.

The robot uses LIDAR for obstacle avoidance and a camera for landmark-based corrections, combined with a reactive path-following controller.

## Key Features
- Extended Kalman Filter for real-time robot state estimation (position + orientation)
- Landmark-based measurement updates using camera recognition
- LIDAR-based obstacle avoidance and goal-directed navigation
- Handles noisy odometry and sensor measurements
- Visualization of uncertainty ellipses during runtime

## Technologies
- **Simulation Environment**: Webots
- **Language**: Python
- **Libraries**: NumPy, SciPy, Matplotlib
- **Key Algorithms**: Extended Kalman Filter (EKF), sensor fusion, reactive navigation

## How It Works
1. **Prediction Step**: Propagates robot state using wheel velocities with process noise
2. **Update Step**: Corrects position estimate using relative landmark positions from camera
3. **Navigation**: Combines goal-heading with LIDAR obstacle avoidance
4. **Visualization**: Real-time plot of estimated position and uncertainty covariance

## Repository Contents
- `final_controller.py` — Main controller with EKF implementation and navigation logic
- `project.wbt` — Webots world file (maze environment for the simulation)
- `video_demo.mp4` — Demonstration video of the robot completing the task

## Setup
Open the project in Webots and run `final_controller.py` as the robot controller.

---

**Homework for the course Sensing and Estimation in Robotics, developed in 2022**
