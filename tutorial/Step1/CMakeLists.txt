cmake_minimum_required(VERSION 3.10)

# set the project name
project(Tutorial VERSION 1.0)

# configure a headerfile to pass version number to code
configure_file(TutorialConfig.h.in TutorialConfig.h)

# set the C++ standard
set(CMAKE_CXX_STANDARD 11)
set(CMAKE_CXX_STANDARD_REQUIRED TRUE)

# Add directory to list of paths to search for include files
target_include_directories(Tutorial PUBLIC
 "${PROJECT_BINARY_DIR}"
)

# add the executable
add_executable(Tutorial tutorial.cxx)

