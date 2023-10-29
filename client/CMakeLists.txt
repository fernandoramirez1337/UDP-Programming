cmake_minimum_required(VERSION 3.0)

project(UDP-client
    VERSION 0.1
	LANGUAGES CXX)
 
set(CMAKE_CXX_STANDARD 11)

find_package(Threads)

set(SOURCES
    source/main.cpp
    source/udp_client.cpp
    ../utilities/source/udp_utilities.cpp)
add_executable(client ${SOURCES})

target_link_libraries (client Threads::Threads )

target_include_directories(client PRIVATE include ../utilities/include)