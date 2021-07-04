add_library(fd_fixed INTERFACE)
target_include_directories(fd_fixed INTERFACE  ${CMAKE_CURRENT_SOURCE_DIR})

add_library(FD::impossibly_fixed ALIAS fd_fixed)

add_executable(benchmark_fixed ${CMAKE_CURRENT_SOURCE_DIR}/DemoEntryPoint.cpp)
target_link_libraries(benchmark_fixed PUBLIC FD::impossibly_fixed)
