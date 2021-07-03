add_library(fd_orig INTERFACE)
target_include_directories(fd_orig INTERFACE 
    ${CMAKE_CURRENT_SOURCE_DIR}/include)

add_library(FD::original ALIAS fd_orig)

add_executable(delegate_demo ${CMAKE_CURRENT_SOURCE_DIR}/demo/delegate_demo.cpp)
target_link_libraries(delegate_demo PUBLIC FD::original)

find_package(Boost 1.25 REQUIRED)

add_executable(event_demo ${CMAKE_CURRENT_SOURCE_DIR}/demo/event_demo1.cpp)
target_link_libraries(event_demo PUBLIC FD::original Boost::headers)

add_subdirectory(test)
add_subdirectory(benchmark)
