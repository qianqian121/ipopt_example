project(ipopt_example)
cmake_minimum_required(VERSION 2.8)

include_directories(/usr/local/include)
link_directories(/usr/local/lib)

add_executable(solver example.cpp)

target_link_libraries(solver ipopt)
