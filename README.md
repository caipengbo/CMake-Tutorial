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

