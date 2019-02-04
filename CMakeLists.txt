cmake_minimum_required(VERSION 3.13)
project(philosophers_dinning)

set(CMAKE_CXX_STANDARD 14)

include_directories(include)

add_executable(philosophers_dinning src/main.cpp include/philosopher.h include/fork.h include/topic.h src/philosopher.cpp src/topic.cpp src/fork.cpp)