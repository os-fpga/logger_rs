cmake_minimum_required(VERSION 3.10)
project(spdlog_examples CXX)

include_directories(${CMAKE_CURRENT_SOURCE_DIR}/spdlog/include)
message(STATUS "spdlog include directory ${CMAKE_CURRENT_SOURCE_DIR}/spdlog/include")
find_package(Threads)
# ---------------------------------------------------------------------------------------
# Example of using header only
# ---------------------------------------------------------------------------------------
add_executable(example example.cpp)
target_link_libraries(example PUBLIC Threads::Threads)

