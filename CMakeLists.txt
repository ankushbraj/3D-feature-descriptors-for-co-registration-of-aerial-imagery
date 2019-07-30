cmake_minimum_required(VERSION 2.8.12)

project(test1)

set(CMAKE_INCLUDE_CURRENT_DIR ON)
set(CMAKE_AUTOMOC ON)

find_package(PCL 1.4 REQUIRED)
find_package(Qt5Core)

include_directories(${PCL_INCLUDE_DIRS})
link_directories(${PCL_LIBRARY_DIRS})
add_definitions(${PCL_DEFINITIONS})

add_executable(${PROJECT_NAME} "main.cpp")

target_link_libraries(${PROJECT_NAME} Qt5::Core)
target_link_libraries (${PROJECT_NAME} ${PCL_LIBRARIES})

set(CMAKE_CXX_STANDARD 17)
