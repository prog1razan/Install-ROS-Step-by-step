# TASK1 : Install-ROS-Step-by-step

What is ROS?
 The Robot Operating System (ROS) is a set of software libraries and tools that help you build robot applications. From drivers to state-of-the-art algorithms, and with powerful developer tools, ROS has what you need for your next robotics project. And it's all open source.
## Table of Contents⚙️
- [Project Description](#project-description)
- [Technologies Used](#technologies-used)
- [Installation](#installation)
- [File Structure](#file-structure)

## Project Description📝
The "Install-ROS-Step-by-step" project provides a comprehensive guide for setting up the Robot Operating System (ROS) on a virtual machine using Oracle VM VirtualBox and Ubuntu 20.04. This guide covers the installation of both ROS Noetic and ROS2 Foxy, ensuring that users can choose and install the version that best fits their needs. The step-by-step instructions are designed to help beginners and experienced developers alike in setting up a robust environment for developing robotics applications.

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
    - For Ubuntu 20.04: https://help.ubuntu.com/community/Installation/SystemRequirements
    - For Ubuntu 20.04 Mate: https://ubuntu-mate.org/about/requirements/
     *We choose Ubuntu 20.04

4. **Setup Ubuntu 20.04 on Virtual Machine**:
     Open VM then enter New and write any name then through ISO image select other and open Ubuntu file.

5. **Setup ROS noetic on Ubuntu 20.04**:
    - Go to https://wiki.ros.org/noetic/Installation and select your platform, we choose Ubuntu.
    - Open Terminal of Ubuntu to write commands to install ROS.
    - Setup your sources.list: Setup your computer to accept software from packages.ros.org.
        ```sh
        sudo sh -c 'echo "deb http://packages.ros.org/ros/ubuntu $(lsb_release -sc) main" > /etc/apt/sources.list.d/ros-latest.list'
        ```
    - Set up your keys:
       ```
        sudo apt install curl # if you haven't already installed curl
       ```
       ```
        curl -s https://raw.githubusercontent.com/ros/rosdistro/master/ros.asc | sudo apt-key add -
       ```
- Make sure your package is up-to-date:
      ```
       sudo apt update
        ```
- Now pick how much of ROS you would like to install: Desktop-Full Install: (Recommended) : Everything in Desktop plus 2D/3D simulators and 2D/3D perception packages.
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
      
- To test if ROS has been installed successfully or not:
     ```
        roscore
    ```
    - if you see meassage contain "SUMMARY" that means you intall ROS noetic successfully and it is running now.
6. **Setup ROS2 foxy on Ubuntu 20.04**:
    - Go to https://docs.ros.org/en/foxy/Installation/Ubuntu-Install-Debians.html .
    - Open Terminal of Ubuntu to write commands to install ROS2 foxy.
    - Set locale:
     ```
     locale  # check for UTF-8
       sudo apt update && sudo apt install locales
       sudo locale-gen en_US en_US.UTF-8
       sudo update-locale LC_ALL=en_US.UTF-8 LANG=en_US.UTF-8
       export LANG=en_US.UTF-8
       locale  # verify settings
     ```
- Setup sources: You will need to add the ROS 2 apt repository to your system
    ```
    sudo apt install software-properties-common
    sudo add-apt-repository universe
    ```
- Now add the ROS 2 GPG key with apt:
```
sudo apt update && sudo apt install curl -y
sudo curl -sSL https://raw.githubusercontent.com/ros/rosdistro/master/ros.key -o /usr/share/keyrings/ros-archive-keyring.gpg
```
- Then add the repository to your sources list:
```
echo "deb [arch=$(dpkg --print-architecture) signed-by=/usr/share/keyrings/ros-archive-keyring.gpg] http://packages.ros.org/ros2/ubuntu $(. /etc/os-release && echo $UBUNTU_CODENAME) main" | sudo tee /etc/apt/sources.list.d/ros2.list > /dev/null
```
- Update your apt repository caches after setting up the repositories:
```
sudo apt update
```
- ROS 2 packages are built on frequently updated Ubuntu systems. It is always recommended that you ensure your system is up to date before installing new packages.
```
sudo apt upgrade
```
- Desktop Install (Recommended): ROS, RViz, demos, tutorials:
```
sudo apt install ros-foxy-desktop python3-argcomplete
```
- Development tools: Compilers and other tools to build ROS packages:
```
sudo apt install ros-dev-tools
```
- Set up your environment by sourcing the following file through nano editor:
```
nano .bashrc
```

```
source /opt/ros/foxy/setup.bash
```
then exit from nano editor by press ctrl x.

- Try some example: If you installed ros-foxy-desktop above you can try some examples.

In one terminal, source the setup file and then run a C++ talker:
```
ros2 run demo_nodes_cpp talker
```
In another terminal source the setup file and then run a Python listener:
```
ros2 run demo_nodes_py listener
```
You should see the talker saying that it’s Publishing messages and the listener saying I heard those messages. This verifies both the C++ and Python APIs are working properly.


## File Structure 🏗️

```
Install-ROS-Step-by-step/
│
├── README.md
```
- `README.md`: This file, containing information about the project.

made with love by "she codes team "🤍😄
raghd Alshammari - sadeem alresaini - razan alothaim.
