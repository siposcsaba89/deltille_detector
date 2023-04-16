find_package(Boost REQUIRED COMPONENTS filesystem program_options system)

add_executable(deltille_detector DeltilleDetector.cpp)
target_link_libraries(deltille_detector deltille Boost::program_options Boost::filesystem)

set_target_properties(deltille_detector PROPERTIES 
  CXX_STANDARD 17
  CXX_STANDARD_REQUIRED ON
)


install(TARGETS deltille_detector DESTINATION ${CMAKE_INSTALL_BINDIR})
