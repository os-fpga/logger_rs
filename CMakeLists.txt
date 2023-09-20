cmake_minimum_required(VERSION 3.10)
project(spdlog_examples CXX)

include_directories(${CMAKE_CURRENT_SOURCE_DIR}/spdlog/include)
message(STATUS "spdlog include directory ${CMAKE_CURRENT_SOURCE_DIR}/spdlog/include")
# ---------------------------------------------------------------------------------------
# Example of using header only
# ---------------------------------------------------------------------------------------
add_executable(example example.cpp)
if(NOT WIN)
  target_link_libraries(example PUBLIC pthread)
else()
  find_package(Threads)
  target_link_libraries(example PUBLIC Threads::Threads)
endif()

