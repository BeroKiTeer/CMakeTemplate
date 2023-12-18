# 设置CMake的最低版本要求
cmake_minimum_required(VERSION 3.20.0)

# 项目名称
project(MyCMakeProject)

# 设置 C++ 标准
set(CMAKE_CXX_STANDARD 20)
set(CMAKE_CXX_STANDARD_REQUIRED ON)

# 添加 include 目录
include_directories(include)

# 查找 src 目录下的所有源文件，并将其存储在变量中
file(GLOB SOURCES "src/*.cpp")

# 添加可执行文件，并将源文件和头文件链接起来
add_executable(main ${SOURCES})

# 如果有其他源文件，可以添加到这里
# add_executable(main ${SOURCES} src/file1.cpp src/file2.cpp)

# 如果需要链接外部库，可以在这里添加
# target_link_libraries(main SomeLibrary)

# 如果需要设置编译选项，可以在这里添加
target_compile_options(main PRIVATE -Wall -O2 -Wextra)
