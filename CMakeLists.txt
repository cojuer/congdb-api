cmake_minimum_required(VERSION 2.8)
project(congdb-api LANGUAGES C CXX)
include(GNUInstallDirs)

set(CMAKE_BUILD_TYPE Debug)
set(CMAKE_CXX_FLAGS "${CMAKE_CXX_FLAGS} -std=c++11 -Wall -Werror")
set(CMAKE_CXX_STANDARD 11)
set (CMAKE_MODULE_PATH ${CMAKE_CURRENT_SOURCE_DIR} ${CMAKE_MODULE_PATH})

find_package(Libnl REQUIRED)
include_directories(BEFORE ${LIBNL_INCLUDE_DIRS})
set(API_SOURCES kernel_api.cpp)
add_library(congdb-api SHARED ${API_SOURCES})

install(TARGETS congdb-api LIBRARY DESTINATION ${CMAKE_INSTALL_LIBDIR})
