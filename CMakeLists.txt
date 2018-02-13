cmake_minimum_required (VERSION 2.6)
project (hello_world)

set (Hello_VERSION_MAJOR 1)


configure_file (
  "${PROJECT_SOURCE_DIR}/HelloConfig.h.in"
  "${PROJECT_BINARY_DIR}/HelloConfig.h"
  )

# add the binary tree to the search path for include files
# so that we will find TutorialConfig.h
include_directories("${PROJECT_BINARY_DIR}")
 
# add the executable
add_executable(HelloWorld hello.cpp)
