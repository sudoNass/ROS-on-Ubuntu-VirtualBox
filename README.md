# ROS-on-Ubuntu-VirtualBox
A guide for installing ROS neotic on ubuntu


## First step: Installing VirtualBox

#### what is VirtualBox?

first i will explain the idea of it for those who have no clue about it so they can understand how it works.

VirtualBox is open-source software for virtualizing the x86 computing architecture. It acts as a hypervisor, creating a VM (virtual machine) where the user can run another OS (operating system).

The operating system where VirtualBox runs is called the "host" OS. The operating system running in the VM is called the "guest" OS. VirtualBox supports Windows, Linux, or macOS as its host OS.

When configuring a virtual machine, the user can specify how many CPU cores, and how much RAM and disk space should be devoted to the VM. When the VM is running, it can be "paused." System execution is frozen at that moment in time, and the user can resume using it later.

#### Downloading Link for VirtualBox

you can download it from thier website by [clicking here!](https://www.virtualbox.org/wiki/Downloads)


now after downloading VirtualBox you can download and run any OS you like through it


## Second step: Downloading Ubuntu

Ubuntu Desktop is a Linux distribution and we need it for our next projects
Ubuntu Desktop will be in disk image format

### System Requirements for Ubuntu
- 4GB RAM or more
- 25GB free disk space

#### Downloading Link for Ubuntu

you can download it from thier website by [clicking here!](https://ubuntu.com/download)


## Third step: Creating a new Virtual Machine

now open VirtualBox then Click "New" Button 

<img width="562" alt="image" src="https://user-images.githubusercontent.com/107954336/176767681-31ee4966-fa10-41eb-809f-2d873ef0247d.png">


and it's gonna ask us for a name so we are going to name it "Ubuntu20.04" or whatever version you have downloaded.

And for Machine Folder you can leave it as default unless you want to save it in a specific location it's up to you

the type we are going to select "Linux" and the version Ubuntu(64-bit)
<img width="561" alt="image" src="https://user-images.githubusercontent.com/107954336/176768419-ea517804-dde5-4098-a20d-ecd02495d7d7.png">


for memory size you need at least 4GB RAM

<img width="560" alt="image" src="https://user-images.githubusercontent.com/107954336/176768667-369e2f5f-efcc-49dc-a056-db27d8f055fe.png">

The next three things we are going to leave it as default

<img width="560" alt="image" src="https://user-images.githubusercontent.com/107954336/176768951-8e6aa1d8-ab03-4eee-896c-0199333bf866.png">   <img width="559" alt="image" src="https://user-images.githubusercontent.com/107954336/176769012-32570a2b-8875-45f8-9307-e04af8599cd2.png">   <img width="558" alt="image" src="https://user-images.githubusercontent.com/107954336/176769076-4c526609-ca83-447b-ad31-d63b7447f0b3.png">


for the disk space at least give it a 25GB

<img width="560" alt="image" src="https://user-images.githubusercontent.com/107954336/176770301-65ce6ac2-1829-4d8f-a28d-9ecdc7e71eb1.png">


## Fourth Step: Modify in the settings

now we have created the Virtual Machine so now we have to modify a few things in the settings
click on Ubuntu then on the settings

<img width="558" alt="image" src="https://user-images.githubusercontent.com/107954336/176771288-f06d5cf3-3234-467b-b500-356bca7574b0.png">


now go to Advanced and make sure those two options are "Bidirectional" so you can be able to copy and paste in and out of it

<img width="608" alt="image" src="https://user-images.githubusercontent.com/107954336/176772043-70cfd070-0e79-4c56-beae-751f15022bf4.png">


next is "System" i'll show you my settings and i recommend the same
(you can max it all through the green area)

<img width="609" alt="image" src="https://user-images.githubusercontent.com/107954336/176772505-7c3d1477-29b9-42e0-a544-d4d691ef983f.png">

in CPU the minimum is 2

<img width="608" alt="image" src="https://user-images.githubusercontent.com/107954336/176772955-ebabe079-2b1e-4280-bf22-d7afbaec5cf3.png">


now in "Display" i'm going to max "Video memory" as well but the default is fine also.

<img width="607" alt="image" src="https://user-images.githubusercontent.com/107954336/176773276-f337a715-37d6-4512-9633-d1d2da371536.png">


now the important part here in the "storage" i'm going to select the empty disk then click on the CD on the right and click on "Choose a disk file" from here we are going to select the ubuntu Image file that we have downloaded 

<img width="610" alt="image" src="https://user-images.githubusercontent.com/107954336/176774223-03211cb4-8029-490b-80f0-6082f9001a7d.png">



and the rest of the settings i'm going to leave it as default

now we are going to select the installation then click on "Start"
in the start-up disk make sure to select the "ubuntu iso image disk" then click start

<img width="509" alt="image" src="https://user-images.githubusercontent.com/107954336/176780672-71e8fd53-55d9-42be-91f6-6b707877c071.png">


next you can select your language then press "Install Ubuntu"

<img width="1025" alt="image" src="https://user-images.githubusercontent.com/107954336/176780869-994fc60a-6be3-405c-8ada-03cb5755cbc8.png">


<img width="690" alt="image" src="https://user-images.githubusercontent.com/107954336/176781084-4211df93-3afb-4190-a761-a73f9af92af6.png">     <img width="695" alt="image" src="https://user-images.githubusercontent.com/107954336/176781184-38892841-7ac2-4183-9344-1a507ef25e4e.png">



Write your name or your computer's name, for username you can change it as you like and set a password and make sure you remember it because you are going to use it a lot as a permission key on Ubuntu.

<img width="1023" alt="image" src="https://user-images.githubusercontent.com/107954336/176781473-213ccafe-13cf-456e-95a1-380334680908.png">

now after the restart we are almost done and we got this desktop but it's a small box, we are going to write a few commands so it fit in the screen like a normal desktop, open the menu and search for "Terminal" from here

<img width="710" alt="image" src="https://user-images.githubusercontent.com/107954336/176782174-cb307dfe-efbc-488a-b766-4a93fad7da15.png">

now in the terminal we will run an update command

```
sudo apt-get update
```

it's going to ask for your password that you have assigned.

now run the upgrade command

```
sudo apt-get upgrade
```

now the last command 

```
sudo apt install build-essential dkms linux-headers-$(uname -r)
```
 
write "Y" if it asked to allow to continue the operation

after finished close the terminal then go to the "Devices" in the menu at the top and select "Insert Guest Additions CD image..."

<img width="1080" alt="image" src="https://user-images.githubusercontent.com/107954336/176783944-d7da8c49-1c06-46da-b90f-1a67cd3b4b68.png">


click on "Run" then type your password then click on "Authenticate"
a window will show up and asks you to press "Enter" to close the window then restart your system.


<img width="1022" alt="image" src="https://user-images.githubusercontent.com/107954336/176784309-414cdcfa-a8ef-4267-87a6-8f7494160df9.png">


after restarting you won't notice anything diffrent until you minimize Ubuntu window then maximize it again then it will fit in your screen, and if you just go to "View" menu and select "Full screen Mode" it will take over the entire screen.

<img width="1080" alt="image" src="https://user-images.githubusercontent.com/107954336/176785179-79b43195-1bc1-4453-9f21-8141953386be.png">


## Fifth step: Install of ROS neotic

this is the last and easiest step for now
you just have to open the terminal again and copy and paste these commands.

Setup your computer to accept software from packages.ros.org by using this command

```
sudo sh -c 'echo "deb http://packages.ros.org/ros/ubuntu $(lsb_release -sc) main" > /etc/apt/sources.list.d/ros-latest.list'
```

Set up your keys

```
sudo apt install curl


curl -s https://raw.githubusercontent.com/ros/rosdistro/master/ros.asc | sudo apt-key add -
```

updating

```
sudo apt-get update
```

ROS distributions are linked to Ubuntu versions:

- Ubuntu 20.04 -> Noetic

- Ubuntu 18.04 -> Melodic

- Ubuntu 16.04 -> Kinetic
    
now i'm using Ubuntu 20.04 so i'll install neotic, you can change "neotic" to one of the above depending on what version you are working with!   
Installing ROS neotic Desktop-Full ,Everything in Desktop plus 2D/3D simulators and 2D/3D perception packages 

```
sudo apt-get install ros-noetic-desktop-full
```
Environment setup
```
echo "source /opt/ros/noetic/setup.bash" >> ~/.bashrc

source ~/.bashrc
```

```
sudo apt install python3-rosdep python3-rosinstall python3-rosinstall-generator python3-wstool build-essential

```

```
sudo apt install python3-rosdep
```

```
sudo rosdep init
```
```
rosdep update
```

```
mkdir -p ~/catkin_ws/src
```

```
cd ~/catkin_ws/
```

```
catkin_make
```

```
cd ~/catkin_ws/src
```

here you can clone any project you want from Github, i will use the Arduino robot arm from Smart-Methods

```
git clone https://github.com/smart-methods/arduino_robot_arm.git 
```

```
cd ~/catkin_ws
```

```
rosdep install --from-paths src --ignore-src -r -y
```

```
sudo apt-get install ros-noetic-moveit
```

```
sudo apt-get install ros-noetic-joint-state-publisher ros-noetic-joint-state-publisher-gui
```

```
sudo apt-get install ros-noetic-gazebo-ros-control joint-state-publisher
```

```
sudo apt-get install ros-noetic-ros-controllers ros-noetic-ros-control
```

```
catkin_make
```
Launching ROS on a project from @Smart_methods for a robotic arm
```
roslaunch robot_arm_pkg check_motors.launch
```

Congrats!! :) everything is set up you can open any project you want 

<img width="540" alt="image" src="https://user-images.githubusercontent.com/107954336/176787831-7a983435-8aca-4f8d-afcd-36c967d1b654.png">


