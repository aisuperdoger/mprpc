cmake_minimum_required(VERSION 3.0)
project(test11)
find_package(PkgConfig REQUIRED)

pkg_check_modules(protobuf REQUIRED IMPORTED_TARGET protobuf)

add_executable(main main.cc test.pb.cc) 
target_link_libraries(main PRIVATE PkgConfig::protobuf)
