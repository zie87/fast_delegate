
add_executable(benchmark 
    ${CMAKE_CURRENT_SOURCE_DIR}/src/benchmark.cpp
    ${CMAKE_CURRENT_SOURCE_DIR}/src/receivers.cpp
    )

target_include_directories(benchmark PUBLIC ${CMAKE_CURRENT_SOURCE_DIR}/src/)
target_link_libraries(benchmark PUBLIC FD::original Boost::headers)
