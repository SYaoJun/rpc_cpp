cmake_minimum_required(VERSION 3.5)
project(buttonrpc LANGUAGES C CXX)
enable_testing()

set(CMAKE_CXX_STANDARD 17)
set(CMAKE_CXX_STANDARD_REQUIRED ON)
set(CMAKE_BUILD_TYPE "Release")

# option(BUILD_UNIT_TESTS "Build unit test" OFF)

# add_library(zmq SHARED zmq.h zmq.hpp)
# set_target_properties(zmq PROPERTIES LINKER_LANGUAGE CXX)
# add_library(rpc SHARED Serializer.hpp buttonrpc.hpp )
# set_target_properties(rpc PROPERTIES LINKER_LANGUAGE CXX)
# add_executable(server main_server.cpp)
# add_executable(client main_client.cpp)

# target_link_libraries(server  rpc zmq)
# target_link_libraries(client  rpc zmq)
add_executable(server main_client.cpp buttonrpc.h Serializer.h zmq_.h zmq.h)
# add_executable(client main_server.cpp buttonrpc.hpp)