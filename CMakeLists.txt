cmake_minimum_required(VERSION 3.3)

project(boost_array)

add_library(boost_array INTERFACE)

target_include_directories(boost_array BEFORE INTERFACE ${CMAKE_CURRENT_SOURCE_DIR}/include)

install(TARGETS boost_array DESTINATION lib)
install(DIRECTORY ${CMAKE_CURRENT_SOURCE_DIR}/include/boost DESTINATION include)

add_library(boost::array ALIAS boost_array)
