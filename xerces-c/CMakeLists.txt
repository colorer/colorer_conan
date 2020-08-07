cmake_minimum_required(VERSION 3.15)

# enable CMAKE_MSVC_RUNTIME_LIBRARY
cmake_policy(SET CMP0091 NEW)

project(cmake_wrapper)


include(conanbuildinfo.cmake)
conan_basic_setup()

add_subdirectory("source_subfolder")
