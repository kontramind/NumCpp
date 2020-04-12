cmake_minimum_required(VERSION 3.15)

# add NumCpp as a 'linkable' target
add_library(NumCpp INTERFACE)

target_include_directories(NumCpp
   SYSTEM
   INTERFACE
   ${CMAKE_CURRENT_LIST_DIR}/include
 )

# provide a namespaced alias for clients to 'link' against if catch is included as a sub-project
add_library(NumCpp::NumCpp ALIAS NumCpp)
