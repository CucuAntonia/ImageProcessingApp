cmake_minimum_required(VERSION 3.0)
project(Algorithms)

set(LibrarySources
	Algorithms.h
	Algorithms.cpp
)

add_definitions(-DALGORITHMS_EXPORT)

add_library(${PROJECT_NAME} SHARED ${LibrarySources})

find_package(OpenCV REQUIRED)
include_directories(${OpenCV_INCLUDE_DIRS})
target_link_libraries(${PROJECT_NAME} ${OpenCV_LIBS})
