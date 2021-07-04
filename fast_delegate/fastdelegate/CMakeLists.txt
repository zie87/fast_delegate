add_library(fd INTERFACE)
target_include_directories(fd INTERFACE ${CMAKE_CURRENT_SOURCE_DIR})
add_library(FD::fastdelegate ALIAS fd)

add_executable(delegate_orig_demo ${CMAKE_CURRENT_SOURCE_DIR}/Demo.cpp)
target_link_libraries(delegate_orig_demo PUBLIC FD::fastdelegate)
