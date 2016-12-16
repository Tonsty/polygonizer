cmake_minimum_required(VERSION 2.8.12)

project(polygonizer)

if(CMAKE_HOST_UNIX)
	# Set a default build type if none was specified
	if(not CMAKE_BUILD_TYPE and not CMAKE_CONFIGURATION_TYPES)
	  message(STATUS "Setting build type to 'Debug' as none was specified.")
	  set(CMAKE_BUILD_TYPE Debug CACHE STRING "Choose the type of build." FORCE)
	  # Set the possible values of build type for cmake-gui
	  set_property(CACHE CMAKE_BUILD_TYPE PROPERTY STRINGS "Debug" "Release"
	    "MinSizeRel" "RelWithDebInfo")
	endif()
endif()

add_executable(polygonizer polygonizer.c)



