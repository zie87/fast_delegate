

add_executable(IncludeTest ${CMAKE_CURRENT_SOURCE_DIR}/src/IncludeTest.cpp)
target_link_libraries(IncludeTest PUBLIC FD::impossibly)
add_executable(IncludeTestP ${CMAKE_CURRENT_SOURCE_DIR}/src/IncludeTestP.cpp)
target_link_libraries(IncludeTestP PUBLIC FD::impossibly)

add_executable(InstanceTest ${CMAKE_CURRENT_SOURCE_DIR}/src/InstanceTest.cpp)
target_link_libraries(InstanceTest PUBLIC FD::impossibly)
add_executable(InstanceTestP ${CMAKE_CURRENT_SOURCE_DIR}/src/InstanceTestP.cpp)
target_link_libraries(InstanceTestP PUBLIC FD::impossibly)

add_executable(MakeTest ${CMAKE_CURRENT_SOURCE_DIR}/src/MakeTest.cpp)
target_link_libraries(MakeTest PUBLIC FD::impossibly)

add_executable(DelegateEventTest ${CMAKE_CURRENT_SOURCE_DIR}/src/DelegateEventTest.cpp)
target_link_libraries(DelegateEventTest PUBLIC FD::impossibly)

find_package(Boost 1.25 REQUIRED)

add_executable(BoostFunctionEventTest ${CMAKE_CURRENT_SOURCE_DIR}/src/BoostFunctionEventTest.cpp)
target_link_libraries(BoostFunctionEventTest PUBLIC FD::impossibly Boost::headers)

add_executable(InterfaceEventTest ${CMAKE_CURRENT_SOURCE_DIR}/src/InterfaceEventTest.cpp)
target_link_libraries(InterfaceEventTest PUBLIC FD::impossibly Boost::headers)
