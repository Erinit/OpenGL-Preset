# 🧊 OpenGL 3D Orbiting Cube

![C++](https://img.shields.io/badge/C++-17-blue.svg?style=flat&logo=c%2B%2B)
![OpenGL](https://img.shields.io/badge/OpenGL-3.3%20Core-5586A4.svg?style=flat&logo=opengl)
![CMake](https://img.shields.io/badge/CMake-Build-success.svg?style=flat&logo=cmake)

A minimalist, modern OpenGL 3.3 project built in C++ that renders a 3D cube with distinctly colored faces. The project features a fully interactive mouse-controlled orbit camera (arcball) and real-time projection toggling.

---

## ✨ Features

* **Modern OpenGL Pipeline:** Uses OpenGL 3.3 Core Profile with custom Vertex and Fragment shaders.
* **Interactive Orbit Camera:** Click and drag the mouse to seamlessly orbit around the 3D object using spherical coordinates and trigonometry.
* **Dynamic Projections:** Toggle between 3D Perspective and isometric Orthographic projections in real-time.
* **Unrolled Geometry:** Demonstrates how to unroll shared vertices to assign unique RGB color attributes to individual faces.
* **Modern CMake Build:** A clean, dependency-friendly `CMakeLists.txt` setup.

---

## 🛠️ Prerequisites & Dependencies

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

Note: If you cloned this repository, the GLAD files are already included in the src/ and include/ directories.

If you are setting this up from scratch, generate the loader files from the GLAD Web Service (C/C++, OpenGL 3.3, Core Profile) and place them in your project structure:

* `glad.c` goes in `src/`

* `glad.h` goes in `include/glad/`

* `khrplatform.h` goes in `include/KHR/`

### How to Build and Run

This project uses an out-of-source CMake build to keep your directory clean. Run the following commands from the root of the project:
```bash
# 1. Create a build directory and navigate into it
mkdir build
cd build

# 2. Configure the project with CMake
cmake ..

# 3. Compile the executable
cmake --build .

# 4. Run the application
./OpenGLRenderer
```

### Project Structure

![STRUCT](images/Screenshot%20From%202026-07-17%2023-26-34.png)
