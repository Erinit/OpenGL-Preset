# OpenGL 3D Orbiting Cube

![C++](https://img.shields.io/badge/C++-17-blue.svg?style=flat&logo=c%2B%2B)
![OpenGL](https://img.shields.io/badge/OpenGL-3.3%20Core-5586A4.svg?style=flat&logo=opengl)
![CMake](https://img.shields.io/badge/CMake-Build-success.svg?style=flat&logo=cmake)

A good preset i believe to set up the openGL specs in yo linux

## Prerequisites & Dependencies

To build this project, you need a **C++17 compiler**, **CMake**, and a few standard graphics libraries. 

This project uses **GLFW** for window creation, **GLM** for 3D mathematics, and **GLAD** for OpenGL extension loading.

### 1. Install System Dependencies (Linux)
It is highly recommended to install the required libraries via your system's package manager.

**Ubuntu / Debian / WSL:**
```bash
sudo apt update
sudo apt install build-essential cmake libglfw3-dev libglm-dev
```

**Fedora**
```bash
sudo dnf install gcc-c++ cmake glfw-devel glm-devel
```

**Arch Linux**
```bash
sudo pacman -S base-devel cmake glfw-x11 glm
```


### 2. GLAD (Extension Loader)

If you are setting this up manually, generate the loader files from the [GLAD Web Service](https://glad.dav1d.de/) (C/C++, OpenGL 3.3, Core Profile) and place them in your project structure:

![I_AM_SO_TIRED](images/Screenshot%20From%202026-07-17%2023-31-14.png)

* `glad.c` goes in `src/`

* `glad.h` goes in `include/glad/`

* `khrplatform.h` goes in `include/KHR/`


### Project Structure

hit these commands
```bash

#made the dir
mkdir -p OpenGLProject/include/KHR OpenGLProject/include/glad OpenGLProject/src


#setting up the files
#note that i wrote code because i have VScode you can change the path of the code
#varaible to any IDE of your linking i think
code OpenGLProject/CMakeLists.txt OpenGLProject/include/KHR/khrplatform.h OpenGLProject/include/glad/glad.h OpenGLProject/src/glad.c OpenGLProject/src/main.cpp

```
press ctrl + o to open the directory alright?


![STRUCT](images/Screenshot%20From%202026-07-17%2023-26-34.png)


### How to Build and Run

Open the project in the 'CMakeLists.txt' hit 'build' make sure theres internet connection and once the build is succesfull hit this cmds
```bash

#in tha directory where the main.cpp is
cd OpenGLProject/src

#hit this to compile the main.cpp with other dependencies whatever
g++ main.cpp glad.c -o my_first_window -I../include -lGL -lglfw

#hit the executable
./my_first_window

```
and i hope you are seeing a cube with multiple colored planes and is orbitable 
now this is a good setup i believe i m thinking of expanding this into a little game
with prebuilt physics libraries or might make a lil physics engine myself

hope this helps
