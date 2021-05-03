# CMake-Tutorial

Fork from https://github.com/ttroy50/cmake-examples

Add my Chinese comments and other additional knowledge.

------
# Summary

# 1. 基础
## A Hello World

三个函数的用法 
```cmake
make_minimum_required()
project()  
add_executable()
```
根据执行cmake输出文件的位置分为两种方式：
1. 当前目录生成
2. 指定输出目录

2种变量：
1. project()会生成变量 ${PROJECT_NAME}
2. ${CMAKE_BINARY_DIR} 执行cmake，也就是cmake输出的目录

## B hello headers

引入其他头文件
target_include_directories
## C 静态库
两种函数
```cmake
add_library(STATIC)
target_link_libraries
```
target_include_directories有三种作用域：PRIVATE, INTERFACE, PUBLIC
target_link_libraries也要作用域，会传播作用域

## D 共享库
add_library(SHARED)
alias别名的使用方法

## E make install

## F CMAKE_BUILD_TYPE
cmake .. -DCMAKE_BUILD_TYPE=Release
- Release - Adds the -O3 -DNDEBUG flags to the compiler
- Debug - Adds the -g flag
- MinSizeRel - Adds -Os -DNDEBUG
- RelWithDebInfo - Adds -O2 -g -DNDEBUG flags

## G CMAKE_CXX_FLAGS

编译FLAGS
set(CMAKE_CXX_FLAGS) 或者通过 cmake .. -DCMAKE_CXX_FLAGS="-DEX3"

## H Third-Party

find_package()

## I 指定编译器

cmake .. -DCMAKE_C_COMPILER=clang-3.6 -DCMAKE_CXX_COMPILER=clang++-3.6
也可以在CMakeLists.txt中使用set进行指定

## L C++ 标准
set(CMAKE_CXX_STANDARD 11)

# 2. 子工程

在最顶层的CMakeLists.txt中使用add_subdirectory()将各个目录(子项目)连接起来，各个子项目之间可以互相引用