project(ipopt_example)
cmake_minimum_required(VERSION 2.8)

message(status "IPOPT_CFLAGS: " ${IPOPT_CFLAGS})
message(status "IPOPT_CFLAGS_OTHER: " ${IPOPT_CFLAGS_OTHER})
set(CMAKE_CXX_FLAGS "-DHAVE_CSTDDEF -DHAVE_MPI_INITIALIZED")

include_directories(/usr/local/include)
link_directories(/usr/local/lib)

add_executable(solver example.cpp)

target_link_libraries(solver ipopt)
