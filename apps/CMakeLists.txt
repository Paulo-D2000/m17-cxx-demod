add_executable(m17-demod m17-demod.cpp)
target_link_libraries(m17-demod PRIVATE m17cxx codec2 Boost::program_options)

add_executable(m17-mod m17-mod.cpp)
target_link_libraries(m17-mod PRIVATE m17cxx codec2 Boost::program_options Threads::Threads)

add_executable(m17-gateway-link m17-gateway-link.cpp)
target_link_libraries(m17-gateway-link PRIVATE m17cxx codec2 Boost::program_options Threads::Threads external)
IF (WIN32)
	target_link_libraries(m17-gateway-link PRIVATE m17cxx wsock32 ws2_32)
ENDIF()

install(TARGETS m17-demod m17-mod m17-gateway-link RUNTIME DESTINATION bin)
