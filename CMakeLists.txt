# CMake 最低版本号要求
cmake_minimum_required(VERSION 3.12)

# 项目信息
project(hello_world)

set(CMAKE_CXX_STANDARD 14)
set(CMAKE_CXX_STANDARD_REQUIRED ON)
set(CMAKE_CXX_EXTENSIONS OFF)

# 指定头文件搜索目录
include_directories(${PROJECT_SOURCE_DIR}/includes)
include_directories(${PROJECT_SOURCE_DIR}/lib/includes)

# 添加 lib 子目录
add_subdirectory(lib)

# 查找src目录下的所有源文件并将名称保存到 DIR_SRCS 变量
aux_source_directory(src DIR_SRCS)

# 指定生成目标
add_executable(${PROJECT_NAME} ${DIR_SRCS})

# 添加链接库
target_link_libraries(${PROJECT_NAME} PUBLIC lib)


