cmake_minimum_required(VERSION 3.10)

# 设置项目名称和版本
project(LearningOpengl VERSION 1.0)

# 设置C++标准
set(CMAKE_CXX_STANDARD 11)
set(CMAKE_CXX_STANDARD_REQUIRED True)

# 找到GLFW库
find_package(glfw3 3.3 REQUIRED)

# 找到OpenGL库
find_package(OpenGL REQUIRED)

# 包含的头文件目录
include_directories(include)

# 添加可执行文件
add_executable(LearningOpengl source/main.cpp source/example.cpp include/test1.hpp include/glad/glad.h
include/KHR/khrplatform.h source/glad.c) 

# 链接GLFW和OpenGL库
target_link_libraries(LearningOpengl glfw ${OPENGL_gl_LIBRARY})