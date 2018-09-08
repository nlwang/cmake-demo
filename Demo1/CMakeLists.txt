#CMakeLists.txt 的语法比较简单，由命令、注释和空格组成，其中命令是不区分大小写的。
#符号 # 后面的内容被认为是注释。命令由命令名称、小括号和参数组成，参数之间使用空格进行间隔。

cmake_minimum_required(VERSION 2.8)

project(Demo1)
set(CMAKE_C_STANDARD 99)

add_executable(${PROJECT_NAME} main.cc)
