cmake_minimum_required(VERSION 3.6)
project(trap_cr3 C CXX)

include(${SOURCE_CMAKE_DIR}/project.cmake)
init_project()

add_vmm_executable(
    trap_cr3	
    LIBRARIES eapis_hve
    LIBRARIES capstone
    SOURCES vmcall_handler.cpp
)
