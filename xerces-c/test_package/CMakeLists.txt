cmake_minimum_required(VERSION 3.15)

# enable CMAKE_MSVC_RUNTIME_LIBRARY
cmake_policy(SET CMP0091 NEW)

project(test_package)

include(${CMAKE_BINARY_DIR}/conanbuildinfo.cmake)
conan_basic_setup()

add_executable(${PROJECT_NAME} test_package.cpp)
target_link_libraries(${PROJECT_NAME} ${CONAN_LIBS})
set_property(TARGET ${PROJECT_NAME} PROPERTY CXX_STANDARD 11)
