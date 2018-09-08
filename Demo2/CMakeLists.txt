# CMake 最低版本号要求
cmake_minimum_required(VERSION 2.8)

# 项目信息
project(Demo2)

# 查找目录下的所有源文件
# 并将名称保存到 DIR_SRCS 变量
aux_source_directory(. DIR_SRCS)

# 指定生成目标
add_executable(${PROJECT_NAME} ${DIR_SRCS})

#唯一的改动只是在 add_executable 命令中增加了一个 MathFunctions.cc 源文件。
#这样写当然没什么问题，但是如果源文件很多，把所有源文件的名字都加进去将是一件烦人的工作。
#更省事的方法是使用 aux_source_directory 命令，该命令会查找指定目录下的所有源文件，然后将结果存进指定变量名。
#其语法如下：aux_source_directory(<dir> <variable>)

#add_executable(${PROJECT_NAME} main.cc MathFunctions.cc)