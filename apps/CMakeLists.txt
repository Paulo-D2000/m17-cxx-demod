add_executable(m17-demod m17-demod.cpp)
target_link_libraries(m17-demod PRIVATE m17cxx codec2 Boost::program_options ../src/tiny-AES-c/tiny-AES-c)

add_executable(m17-mod m17-mod.cpp)
target_link_libraries(m17-mod PRIVATE m17cxx codec2 Boost::program_options Threads::Threads ../src/tiny-AES-c/tiny-AES-c)

install(TARGETS m17-demod m17-mod RUNTIME DESTINATION bin)
