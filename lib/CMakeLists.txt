# 项目信息
project(lib)

# 指定头文件搜索目录
include_directories(${PROJECT_SOURCE_DIR}/includes)

# 查找src目录下的所有源文件并将名称保存到 DIR_SRCS 变量
aux_source_directory(src DIR_SRCS)

# 生成链接库
add_library(${PROJECT_NAME} ${DIR_SRCS})
