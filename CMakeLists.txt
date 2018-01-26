cmake_minimum_required(VERSION 3.9)
project(airwindows_ports)

set(CMAKE_CXX_STANDARD 14)
add_definitions(-D__cdecl=)

include(Helpers.cmake)

add_subdirectory(include/vstsdk)
add_airwindows_plugin(BitShiftGain)
add_airwindows_plugin(PurestConsoleBuss)
add_airwindows_plugin(PurestConsoleChannel)
add_airwindows_plugin(PurestGain)
add_airwindows_plugin(TPDFDither)
