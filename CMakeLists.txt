cmake_minimum_required(VERSION 2.8)

project(UMP C)

include_directories(include)

add_subdirectory(src)
add_subdirectory(include)

configure_file(libUMP.pc.in libUMP.pc @ONLY)

install(FILES ${CMAKE_CURRENT_BINARY_DIR}/libUMP.pc DESTINATION lib/pkgconfig)
