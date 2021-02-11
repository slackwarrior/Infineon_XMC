cmake_minimum_required(VERSION 3.10)

#Project name
project(XMC_CMake_Environment 
	VERSION 0.0.1
	DESCRIPTION "Sample project for compiling code for XMC microcontrollers; these chips are very interesting, industrial grade, 5V supplied, but have weak support for Linux - I could fix it, with this piece of code"
	LANGUAGES C)

set(CMAKE_SYSTEM_NAME generic)
set(CMAKE_SYSTEM_PROCESSOR arm)

set(CMAKE_SYSROOT /home/devel/rasp-pi-rootfs)
set(CMAKE_STAGING_PREFIX /home/devel/stage)

set(tools /home/karol/bin/gcc-arm-none-eabi-9-2019-q4-major/bin)
set(CMAKE_C_COMPILER ${tools}/arm-none-eabi-gcc)
set(CMAKE_CXX_COMPILER ${tools}/arm-none-eabi-g++)

set(CMAKE_FIND_ROOT_PATH_MODE_PROGRAM NEVER)
set(CMAKE_FIND_ROOT_PATH_MODE_LIBRARY ONLY)
set(CMAKE_FIND_ROOT_PATH_MODE_INCLUDE ONLY)
set(CMAKE_FIND_ROOT_PATH_MODE_PACKAGE ONLY)

#main executable
add_executable(run_main src/main.c)
