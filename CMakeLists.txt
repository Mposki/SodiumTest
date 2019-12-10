cmake_minimum_required(VERSION 2.8)

project(TestCMake)

list(APPEND CMAKE_MODULE_PATH "${CMAKE_CURRENT_SOURCE_DIR}/cmake")
find_package(sodium)

message(STATUS "sodium_FOUND: ${sodium_FOUND}")
message(STATUS "sodium_INCLUDE_DIR: ${sodium_INCLUDE_DIR}")
message(STATUS "sodium_LIBRARY_DEBUG: ${sodium_LIBRARY_DEBUG}")
message(STATUS "sodium_LIBRARY_RELEASE: ${sodium_LIBRARY_RELEASE}")
message(STATUS "sodium_VERSION_STRING: ${sodium_VERSION_STRING}")


add_executable(${PROJECT_NAME} "main.cpp")

target_link_libraries(${PROJECT_NAME} ${sodium_LIBRARY_DEBUG})
