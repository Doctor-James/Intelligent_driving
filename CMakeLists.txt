cmake_minimum_required(VERSION 2.8)
project(Intelligent_driving)

set(CMAKE_CXX_STANDARD 11)

find_package( OpenCV REQUIRED )

include_directories(${OpenCV_INCLUDE_DIRS})

add_executable(Intelligent_driving src/main.cpp 
        src/common/rvec2elur.h src/common/rvec2elur.cpp
        src/common/codeRotate.h src/common/rotate.cpp src/park/Park.h
        src/park/Park.cpp serial/Serial.h serial/Serial.cpp src/auto_drive/autodrive.h src/auto_drive/autodrive.cpp)

target_link_libraries(Intelligent_driving ${OpenCV_LIBS} )