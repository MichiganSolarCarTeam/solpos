cmake_minimum_required(VERSION 3.20 FATAL_ERROR)

project(
        solpos
        VERSION 1.0
        LANGUAGES CXX
)

# Create Libraries
add_library(solpos_solpos STATIC)
add_library(solpos::solpos ALIAS solpos_solpos)

# Add Sources
target_sources(
        solpos_solpos
        PRIVATE solpos.c
        PUBLIC solpos.h
)
set_target_properties(solpos_solpos PROPERTIES LINKER_LANGUAGE CXX)
