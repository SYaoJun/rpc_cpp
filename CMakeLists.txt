cmake_minimum_required(VERSION 3.5)
project(buttonrpc LANGUAGES C CXX)
enable_testing()

set(CMAKE_CXX_STANDARD 17)
set(CMAKE_CXX_STANDARD_REQUIRED ON)
set(CMAKE_BUILD_TYPE "Release")


add_executable(server main_server.cpp )
add_executable(client main_client.cpp )
target_link_libraries(server /usr/local/lib/libzmq.so.5)
target_link_libraries(client /usr/local/lib/libzmq.so.5)