cmake_minimum_required(VERSION 3.5)

project(typeye_console LANGUAGES CXX)

set(CMAKE_INCLUDE_CURRENT_DIR ON)

set(CMAKE_AUTOUIC ON)
set(CMAKE_AUTOMOC ON)
set(CMAKE_AUTORCC ON)

set(CMAKE_CXX_STANDARD 11)
set(CMAKE_CXX_STANDARD_REQUIRED ON)
SET(OpenCV_DIR "/installation/OpenCV/lib/cmake/opencv4")
SET(OpenCV_LIBS "/installation/OpenCV/lib/")

find_package(Qt5Core)
find_package(OpenCV)

add_executable(typeye_console main.cpp)
target_link_libraries(typeye_console Qt5::Core)

include_directories( ${OpenCV_INCLUDE_DIRS} )
target_link_libraries( typeye_console ${OpenCV_LIBS} )

