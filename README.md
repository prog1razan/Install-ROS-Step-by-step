# TASK1 : Install-ROS-Step-by-step

What is ROS?
 The Robot Operating System (ROS) is a set of software libraries and tools that help you build robot applications. From drivers to state-of-the-art algorithms, and with powerful developer tools, ROS has what you need for your next robotics project. And it's all open source.
## Table of Contents⚙️
- [Project Description](#project-description)
- [Technologies Used](#technologies-used)
- [Installation](#installation)
- [File Structure](#file-structure)

## Project Description📝


## Technologies Used 🔧

- **Oracle VM Virtual Box**:
- **Ubuntu 20.04**:

## Installation 🗺️

1. **Download VM**:
    https://www.virtualbox.org/wiki/Downloads

2. **Download Ubuntu 20.04 or Ubuntu mate 20.04**:
    - To download Ubuntu 20.04: https://releases.ubuntu.com/20.04/
    - To download Ubuntu 20.04 Mate: https://releases.ubuntu-mate.org/20.04/amd64/

3. **Create the Virtual Machine**:
    - see the system requirements:
     -For Ubuntu 20.04: https://help.ubuntu.com/community/Installation/SystemRequirements
     -For Ubuntu 20.04 Mate: https://ubuntu-mate.org/about/requirements/
     *We choose Ubuntu 20.04

4. **Setup Ubuntu 20.04 on Virtual Machine**:
     Open VM then enter New and write any name then through ISO image select other and open Ubuntu file.

5. **Setup ROS on Ubuntu 20.04**:
    - Go to https://wiki.ros.org/noetic/Installation and select your platform, we choose Ubuntu.
    - Open Terminal of Ubuntu to write commands to install ROS.
    - Setup your sources.list: Setup your computer to accept software from packages.ros.org.
        ```sh
        sudo sh -c 'echo "deb http://packages.ros.org/ros/ubuntu $(lsb_release -sc) main" > /etc/apt/sources.list.d/ros-latest.list'
        ```
    - Set up your keys:
       ```
        sudo apt install curl # if you haven't already installed curl
curl -s https://raw.githubusercontent.com/ros/rosdistro/master/ros.asc | sudo apt-key add -
        ```
- Make sure your package is up-to-date:
        ```
       sudo apt update
        ```
- Now pick how much of ROS you would like to install: 
      -Desktop-Full Install: (Recommended) : Everything in Desktop plus 2D/3D simulators and 2D/3D perception packages
        ```
        sudo apt install ros-noetic-desktop-full
        ```
- There are even more packages available in ROS. You can always install a specific package directly.
        ```
        sudo apt install ros-noetic-PACKAGE
        ```
        e.g.
        ```
        sudo apt install ros-noetic-slam-gmapping
        ```
- To find available packages, see https://index.ros.org/packages/page/1/time/#noetic or use:
       ```
        apt search ros-noetic
        ```
- You must source this script in every bash terminal you use ROS in:
     ```
        source /opt/ros/noetic/setup.bash
      ```
- To test if ROS has been installed successfully or not:
     ```
        roscore
    ```
if you see meassage contain "summary" that means you intall ROS successfully and it is running now.




## File Structure 🏗️

```
Install-ROS-Step-by-step/
│
├── README.md
```
- `README.md`: This file, containing information about the project.

made with love by "she codes team "🤍😄
raghd Alshammari - sadeem alresaini - razan alothaim.
