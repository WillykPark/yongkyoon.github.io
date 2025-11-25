---
layout: project
title: 'Robot Arm Control'
caption: Robot Arm control Project.
description: >
  This study presents a ROS 2-based framework for controlling a robotic arm using a haptic glove as an input interface.
  The system enables real-time motion mapping to achieve accurate and responsive manipulation.
date: 24 Apr 2025
image: 
  path: /assets/img/projects/robot_arm.png
  srcset: 
    1920w: /assets/img/projects/robot_arm.png
    960w:  /assets/img/projects/robot_arm@0,5x.png
    480w:  /assets/img/projects/robot_arm@0,25x.png
links:
  - title: Link
    url: https://github.com/WillykPark/RobotArm_Control_Project.git
accent_color: '#4fb1ba'
accent_image:
  background: '#193747'
theme_color: '#193747'
sitemap: false
---

This project enables real-time teleoperation of a simulated robotic arm using a haptic glove. The glove transmits spatial and finger position data over Wi-Fi, which is consumed by a ROS 2 node that controls a simulated robot arm in PyBullet. The architecture supports full simulation, testing on a single PC without ROS, or mocking the glove input.

```yml
haptic_glove_robot_arm/
├── haptic_glove_robot_arm/          # ROS 2 package (main integration)
│   ├── glove_publisher.py           # ROS node: receives glove data via socket, publishes to /glove_data
│   ├── arm_subscriber.py           # ROS node: subscribes to /glove_data, simulates arm in PyBullet
│
├── haptic_glove_robot_arm_mock/     # Standalone scripts (no ROS)
│   ├── glove_arm_simulator_no_ros.py # Direct glove-to-arm simulation via serial
│   ├── glove_publisher_mock.py      # Mock publisher node for testing without hardware
│
├── haptic_glove_setup/              # Setup scripts for glove device
│   ├── glove_arduino_setup.ino      # Arduino firmware for glove
│   ├── glove_data_wifi_transition.py # Reads serial glove data, sends to ROS node over Wi-Fi
│
├── test/                            # Code quality tests
├── demo/                            # Folder with the banner of the project and a demo
├── resource/, LICENSE, setup.py, etc.
```

<!-- The configuration I use to enable the system font on my site. Feel free to copy!
{:.figcaption} -->
