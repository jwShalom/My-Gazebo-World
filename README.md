# My-Gazebo-World
Welcome to *My Gazebo World* - a captivating Gazebo simulation that brings the virtual and real worlds together! This project combines the power of Gazebo's robust simulation environment with real-life objects, allowing you to experience an immersive and interactive simulation. This world involves an apartment floor space, furnitures and robots. In addition, this project allows you to interact with Gazebo plugins 


## Purpose 
+ Demonstrate an ability to use a **building editor** tool in Gazebo. Apply different feature, color and texture on the structure (building) and design a space that's enough for a robot to navigate.
+ Model various objects that resembles a real-life object and a robot through **model editor** tool in Gazebo. A robot components should also be connect with joints.
+ Import a struture and objects that I created and from the Gazebo online library to an empty Gazebo world.
+ Write a **C++ plugin** to interact with my world. It will display a welcome message "Hello! Welcome to my Gazebo workspace!" as I launch my Gazebo world file through a terminal.

## Directory

```C++
    My_Gazebo_World                       # Build a project directory 
       ├── model                          # Model files 
       │   ├── 4_wheeled_robot              #Robot file
       │   │   ├── model.config
       │   │   ├── model.sdf
       │   ├── table                        #Table file
       │   │   ├── model.config
       │   │   ├── model.sdf
       │   ├── chair                        #Chair file
       │   │   ├── model.config
       │   │   ├── model.sdf
       │   ├── Naegok_House                 #House(structure) file
       │   │   ├── model.config
       │   │   ├── model.sdf
       ├── script                         # Gazebo World plugin C++ script      
       │   ├── hello_plugin.cpp
       ├── world                          # Gazebo main World containing models 
       │   ├── Gazebo_World_Project.world
       ├── CMakeLists.txt                 # Link libraries 
       └── 

```

## How to launch the simulation
1. Update and upgrade the Workspace image
   ```Bash
   $ sudo apt-get update && sudo apt-get upgrade -y
   ```
2. Clone the project folder in your workspace
   ```Bash
   $ cd /home/<name of your workspace: workspace (for example)>/
   $ git clone https://github.com/jwShalom/My-Gazebo-World/
   ```
3. Remove the build folder
   ```Bash
   rm -rf build
   ```
4. Compile the code
   ```Bash
   $ cd /home/workspace/My-Gazebo-World
   $ mkdir build
   $ cd build/
   $ cmake ../
   $ make
   ```
5. Add the library path to the Gazebo plugin path
   ```Bash
   $ export GAZEBO_PLUGIN_PATH=${GAZEBO_PLUGIN_PATH}:/home/<user name>/workspace/My-Gazebo-World/build
   ```
6. Run the Gazebo World file
  ```Bash
   $ cd /home/workspace/My-Gazebo-World/world/
   $ gazebo Gazebo_World_Project
  ```

Done!
![Screenshot 2023-07-17 184129](https://github.com/jwShalom/My-Gazebo-World/assets/124924697/5ae785d9-81a8-43e7-9c4b-8a39c7d9baa4)
