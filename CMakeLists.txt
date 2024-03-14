cmake_minimum_required(VERSION 3.0.0)
project(demo VERSION 0.1.0 LANGUAGES C CXX)

include(CTest)
enable_testing()



# 查找当前目录下的所有源文件
# 并将名称保存到 DIR_SRCS 变量
aux_source_directory(. DIR_SRCS)
add_executable(dedemo ${DIR_SRCS})

add_executable(demo main.cpp)
#add_executable(${PROJECT_NAME} main.cpp)


set(CPACK_PROJECT_NAME ${PROJECT_NAME})
set(CPACK_PROJECT_VERSION ${PROJECT_VERSION})
include(CPack)
