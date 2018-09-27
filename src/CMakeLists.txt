cmake_minimum_required(VERSION 2.8)

add_library(UMP SHARED ump_arch.c ump_frontend.c ump_osu_locks.c ump_osu_memory.c
	ump_ref_drv.c ump_uku.c)

set_target_properties(UMP PROPERTIES VERSION 3.0.0 SOVERSION 3)

target_link_libraries(UMP m dl)

install(TARGETS UMP LIBRARY DESTINATION lib ARCHIVE DESTINATION lib)
