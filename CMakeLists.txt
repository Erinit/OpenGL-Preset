cmake_minimum_required(VERSION 3.14)
project(OpenGLRenderer)

set(CMAKE_CXX_STANDARD 17)
set(CMAKE_CXX_STANDARD_REQUIRED ON)

# 1. Create the Executable
add_executable(${PROJECT_NAME} 
    src/main.cpp 
    src/glad.c
)

# 2. Include GLAD headers
target_include_directories(${PROJECT_NAME} PRIVATE include)

# 3. Find system libraries (No downloading required)
find_package(OpenGL REQUIRED)
find_package(glfw3 REQUIRED)
find_package(glm REQUIRED)

# 4. Link everything together
target_link_libraries(${PROJECT_NAME} PRIVATE 
    glfw 
    glm 
    OpenGL::GL
)