# PID Controller for DC Motor with ROS and Arduino

## Overview

This project implements a PID controller for a direct current (DC) motor using ROS (Robot Operating System) and Arduino. The project has been developed in collaboration with Manchester Robotics.

## Requirements

- ROS framework.
- Arduino IDE.

## Hardware Setup

1. Connect the DC motor to the Arduino.
2. Upload the ```arduino_code/final_challenge_arduino.ino``` code to the Arduino using the Arduino IDE.

## Software Setup

1. Clone this repository into your workspace's `src` directory (e.g., `catkin_ws/src/`):
    ```bash
    git clone <repository_url>
    ```

2. Navigate to your workspace directory (e.g., `catkin_ws`) and execute `catkin_make` to compile the package:
    ```bash
    cd catkin_ws
    catkin_make
    ```

3. Once compiled, set up your ROS workspace:
    ```bash
    source devel/setup.bash
    ```

## Usage

1. To run the PID controller, execute the `final.launch` file using the following command:
    ```bash
    roslaunch ROS_code final.launch
    ```

2. After running `final.launch`, the PID controller will be active.

3. Change the parameters file to adjust the PID mode in `setPoint_file.yaml`:
    - `op`: Operation mode from 1 to 4. Where:
        1. Square signal
        2. Sinusoidal signal
        3. Linear signal
        4. Keyboard input, "A" for forward and "D" for backward
    - `period`
    - `vel`: Velocity

4. Change the PID constants in `control_file.yaml`.

## Demo

For a visual demonstration of the project, you can watch the following video:

[![Project Demo](http://img.youtube.com/vi/BHTzVF8sD1Q/0.jpg)](https://www.youtube.com/watch?v=BHTzVF8sD1Q)
