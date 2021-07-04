
add_executable(benchmark_orig 
    ${CMAKE_CURRENT_SOURCE_DIR}/src/benchmark.cpp
    ${CMAKE_CURRENT_SOURCE_DIR}/src/receivers.cpp
    )

target_include_directories(benchmark_orig PUBLIC ${CMAKE_CURRENT_SOURCE_DIR}/src/)
target_link_libraries(benchmark_orig PUBLIC FD::impossibly Boost::headers)
