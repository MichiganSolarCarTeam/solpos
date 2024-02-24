cmake_minimum_required(VERSION 3.20 FATAL_ERROR)

project(
        solpos
        VERSION 1.0
        LANGUAGES CXX
)

# Create Libraries
add_library(solpos_solpos INTERFACE)
add_library(solpos::solpos ALIAS solpos_solpos)
set_property(TARGET solpos_solpos PROPERTY EXPORT_NAME solpos)

# Add include directories
target_include_directories(solpos_solpos
        INTERFACE
        $<BUILD_INTERFACE:${PROJECT_SOURCE_DIR}/include>
)

