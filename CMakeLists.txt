cmake_minimum_required(VERSION 3.10)

#Project name
project(XMC_CMake_Environment 
	VERSION 0.0.1
	DESCRIPTION "Sample project for compiling code for XMC microcontrollers; these chips are very interesting, industrial grade, 5V supplied, but have weak support for Linux - I could fix it, with this piece of code"
	LANGUAGES C)

#main executable
add_executable(run_main src/main.c)
