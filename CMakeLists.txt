cmake_minimum_required (VERSION 2.6)
project (SDL_OGL)

SET(CMAKE_CXX_FLAGS "-g")

# The version number.
set (SDL_OGL_VERSION_MAJOR 1)
set (SDL_OGL_VERSION_MINOR 1)
 
# configure a header file to pass some of the CMake settings
# to the source code
configure_file (
  "${PROJECT_SOURCE_DIR}/SDL_OGLConfig.h.in"
  "${PROJECT_BINARY_DIR}/SDL_OGLConfig.h"
  )
 
# add the binary tree to the search path for include files
# so that we will find SDL_OGL_Config.h
include_directories("${PROJECT_BINARY_DIR}")

 add_subdirectory (src) 
 
