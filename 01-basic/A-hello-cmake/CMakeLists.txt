# Set the minimum version of CMake that can be used
# To find the cmake version run
# $ cmake --version
cmake_minimum_required(VERSION 3.5)

# Set the project name
project(hello_cmake)  # 会产生${PROJECT_NAME}变量

# Add an executable
add_executable(hello_cmake main.cpp)  # 第一个参数是可执行文件的名字，第二个参数是源文件列表
