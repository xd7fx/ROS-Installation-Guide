# ROS Installation Guide using VirtualBox and Ubuntu 20.04

This guide provides step-by-step instructions to install ROS (Robot Operating System) on a virtual machine using VirtualBox and Ubuntu 20.04.

## Table of Contents

- [Prerequisites](#prerequisites)
- [Step 1: Download and Install VirtualBox](#step-1-download-and-install-virtualbox)
- [Step 2: Download Ubuntu 20.04 Desktop Image](#step-2-download-ubuntu-20.04-desktop-image)
- [Step 3: Create a New Virtual Machine in VirtualBox](#step-3-create-a-new-virtual-machine-in-virtualbox)
- [Step 4: Install Ubuntu 20.04](#step-4-install-ubuntu-20.04)
- [Step 5: Install ROS on Ubuntu 20.04](#step-5-install-ros-on-ubuntu-20.04)
- [Step 6: Problems installing ROS and their solutions](#Step-6-Problems-installing-ROS-and-their-solutions)

## Prerequisites

- A computer with internet access.
- Basic knowledge of using the command line.

## Step 1: Download and Install VirtualBox

1. Open your web browser and go to the [VirtualBox website]
([https://www.virtualbox.org/](https://www.virtualbox.org/wiki/Downloads )).

![لقطة الشاشة 2024-07-10 213750](https://github.com/xd7fx/ROS-Installation-Guide/assets/173664349/b5f453f3-de08-4964-85cd-c55fa23e62c5)
2. Click on "Download VirtualBox".
3. Select the version appropriate for your operating system (Windows, macOS, Linux).
4. After downloading, open the installation file and follow the on-screen instructions to install VirtualBox.

## Step 2: Download Ubuntu 20.04 Desktop Image

1. Open your web browser and go to the [Ubuntu website](https://ubuntu.com/download/desktop).
![لقطة الشاشة 2024-07-09 164728](https://github.com/xd7fx/ROS-Installation-Guide/assets/173664349/e9328bd9-7ded-436a-b1fa-4c4f990956e7)
2. Select "Ubuntu 20.04 LTS" and click on "Download".
3. Save the ISO file to your computer.

## Step 3: Create a New Virtual Machine in VirtualBox

1. Open VirtualBox and click on "New" to create a new virtual machine.
![لقطة الشاشة 2024-07-09 164747](https://github.com/xd7fx/ROS-Installation-Guide/assets/173664349/aa04a273-25fc-4623-8c64-f798736bb4ad)

2. Name the machine (e.g., "Ubuntu 20.04") and choose the type of operating system as "Linux" and the version as "Ubuntu (64-bit)".
![لقطة الشاشة 2024-07-09 164801](https://github.com/xd7fx/ROS-Installation-Guide/assets/173664349/8175b882-65f5-40bc-af83-2fb1acdcefc3)

3. Set the memory size (RAM) (at least 2 GB is recommended)(to green).
![لقطة الشاشة 2024-07-09 164841](https://github.com/xd7fx/ROS-Installation-Guide/assets/173664349/860072dc-9bb2-4e07-a24a-515c097cc4bd)
4. Set the size of the virtual hard disk (at least 25 GB is recommended) and click "Create".
![لقطة الشاشة 2024-07-09 164855](https://github.com/xd7fx/ROS-Installation-Guide/assets/173664349/36cd8ab4-01a5-4a18-ab04-95fa7c3f174d)

## Step 4: Install Ubuntu 20.04

1. After creating the virtual machine, select it from the list in VirtualBox and click "Start".
![لقطة الشاشة 2024-07-09 164909](https://github.com/xd7fx/ROS-Installation-Guide/assets/173664349/c992f120-f2bd-4d85-ac8a-cb7de3af254b)

2. When prompted, choose the Ubuntu 20.04 ISO file you downloaded and click "Start".
![لقطة الشاشة 2024-07-09 164958](https://github.com/xd7fx/ROS-Installation-Guide/assets/173664349/f49c9cc9-aa4a-4c84-abc8-957fc7af9b3e)
![لقطة الشاشة 2024-07-09 165022](https://github.com/xd7fx/ROS-Installation-Guide/assets/173664349/9d609fd1-3e88-47b6-a9f8-c5a7b841e70f)

3. Follow the on-screen instructions to install Ubuntu 20.04 on the virtual machine.
![لقطة الشاشة 2024-07-09 165045](https://github.com/xd7fx/ROS-Installation-Guide/assets/173664349/ee466962-875c-46a8-98bd-bae49f50e3d1)
4. Choose the third option install Ubuntu

![لقطة الشاشة 2024-07-09 165115](https://github.com/xd7fx/ROS-Installation-Guide/assets/173664349/3ed577ad-0279-4eb5-b826-d18a8bf32dba)
![لقطة الشاشة 2024-07-09 165235](https://github.com/xd7fx/ROS-Installation-Guide/assets/173664349/94e1a890-4475-4ef3-8e5c-47be22026256)
![لقطة الشاشة 2024-07-09 165313](https://github.com/xd7fx/ROS-Installation-Guide/assets/173664349/e8a572eb-9bba-4cd7-a9b0-8fbeab9390ad)

5.Important thing, turn off the “Download updates while installing Ubuntu” option so that it does not update Ubuntu 20.04
![لقطة الشاشة 2024-07-09 165419](https://github.com/xd7fx/ROS-Installation-Guide/assets/173664349/07b3c9c8-2dba-4119-8c23-503b1cd0c362)
![لقطة الشاشة 2024-07-09 165512](https://github.com/xd7fx/ROS-Installation-Guide/assets/173664349/c07bd209-bc29-4563-8951-b2e5a4cf7444)
![لقطة الشاشة 2024-07-09 165618](https://github.com/xd7fx/ROS-Installation-Guide/assets/173664349/0ac4719d-2c13-4469-a08b-d672ddf13b0b)



## Step 5: Install ROS on Ubuntu 20.04

1. After installing and booting Ubuntu, open a terminal window.
![لقطة الشاشة 2024-07-10 070133](https://github.com/xd7fx/ROS-Installation-Guide/assets/173664349/92bacad6-ccd2-4f20-b884-0812b1c21af2)

2. Add the ROS repository to your system:
    ```bash
    sudo sh -c 'echo "deb http://packages.ros.org/ros/ubuntu $(lsb_release -sc) main" > /etc/apt/sources.list.d/ros-latest.list'
    ```
![لقطة الشاشة 2024-07-10 214513](https://github.com/xd7fx/ROS-Installation-Guide/assets/173664349/00e6a102-d09f-4ae8-ab94-fb886f772777)

3. Add the ROS key:
    ```bash
    sudo apt install curl
    curl -s https://raw.githubusercontent.com/ros/rosdistro/master/ros.asc | sudo apt-key add -
    ```
![لقطة الشاشة 2024-073-10 221346](https://github.com/xd7fx/ROS-Installation-Guide/assets/173664349/748c6736-826e-4203-aa75-ece5ee3f2a57)

4. Update the package list:
    ```bash
    sudo apt update
    ```
![لقطة الشاشة 2024-027-10 221346](https://github.com/xd7fx/ROS-Installation-Guide/assets/173664349/f60d6971-22f7-4cff-81c9-6c263cf187a9)

5. Install the full version of ROS (Noetic):
  
    ```bash
    sudo apt install ros-noetic-desktop-full
    ```
- "If you get a problem like the one I have, go to step 6, solve the problem, and go back and complete the installation. If you don’t get a problem, complete the installation."
- [Step 6: Problems installing ROS and their solutions](#Step-6-Problems-installing-ROS-and-their-solutions)
   ![لقطة الشاشة 32024-07-10 214401](https://github.com/xd7fx/ROS-Installation-Guide/assets/173664349/3798871b-a203-4306-a33c-38d06af1a882)
-no error
 ![لقطة الشاشة 2024-07-10 222529](https://github.com/xd7fx/ROS-Installation-Guide/assets/173664349/e7808af2-09fe-472f-9e6e-f158969c0d7e)
  ![لقطة الشاشة 2024-07-10 212600](https://github.com/xd7fx/ROS-Installation-Guide/assets/173664349/07d6a9cc-813a-413c-b427-7f2817427c77)

 
7. Set up the ROS environment:
    ```bash
    echo "source /opt/ros/noetic/setup.bash" >> ~/.bashrc
    source ~/.bashrc
    ```
![لقطة الشاشة 2024-07-10 222655](https://github.com/xd7fx/ROS-Installation-Guide/assets/173664349/25d52c86-77bc-4952-93ad-e04bd54068cb)


Congratulations! ROS is now successfully installed on Ubuntu 20.04 within VirtualBox. You can start using ROS to develop robotics applications.

## Step 6: Problems installing ROS and their solutions
1. go to settings and go About and Software Updates
![لقطة الشاشة 2024-07-10 222826](https://github.com/xd7fx/ROS-Installation-Guide/assets/173664349/3fb62e63-502a-4342-8ed1-31e6b6a06d68)

2. Make sure this setting is set
![لقطة الشاشة 2024-07-10 212421](https://github.com/xd7fx/ROS-Installation-Guide/assets/173664349/43d02446-130d-414e-8d95-382c66aebf5a)
3. Go to (Terminal) and place these commands in this order
   ```bash
    sudo apt clean
    ```
   ```bash
    sudo apt autoclean
    ```
   ```bash
    sudo apt autoremove
    ```
   ```bash
    sudo apt update
    ```
   ```bash
    sudo dpkg --configure -a
    ```
   ```bash
    sudo apt install -f
    ```
![لقطة الشاشة 2024-07-10 223720](https://github.com/xd7fx/ROS-Installation-Guide/assets/173664349/1733dea1-a731-4095-b914-5fd707bd643e)

   ```bash
    sudo apt upgrade
```
![لقطة الشاشة 2024-07-10 223951](https://github.com/xd7fx/ROS-Installation-Guide/assets/173664349/0d3a3820-585c-4efb-8f6c-23f714963cda)

4. Now start from the beginning and everything will be fine
![لقطة الشاشة 2024-07-10 224203](https://github.com/xd7fx/ROS-Installation-Guide/assets/173664349/338df0c4-a6cd-4f57-8cbb-82c7d4870bfd)






   






