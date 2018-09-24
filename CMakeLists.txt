if(CMAKE_SOURCE_DIR EQUAL CMAKE_BINARY_DIR)
	message(FATAL_ERROR "Builds within the source directory are not allowed!")
endif()

cmake_minimum_required (VERSION 3.7)

set (PROJECT_NAME project_name)
project (${PROJECT_NAME})

if(NOT CMAKE_BUILD_TYPE)
	set(CMAKE_BUILD_TYPE "Release" CACHE STRING "Choose the build type, 
		options are: None, Debug, Release, RelWithDebInfo, MinSizeRel." FORCE)
endif()

set(CMAKE_MODULE_PATH ${CMAKE_MODULE_PATH} "${CMAKE_SOURCE_DIR}/cmake/Modules/")

set(CMAKE_CXX_STANDARD 14)

if(CMAKE_COMPILER_IS_GNUCXX)
	set(CMAKE_CXX_FLAGS "${CMAKE_CXX_FLAGS} -Wall")
endif()

add_subdirectory(src/library)
add_subdirectory(src)

option(WITH_GUI "With Graphical User Interface" OFF)
if(WITH_GUI)
	add_subdirectory(src/gui)
endif()
