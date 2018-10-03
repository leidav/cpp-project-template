add_executable(executable_name main.cpp)
#target_sources(executable_name PRIVATE 
#               "${CMAKE_CURRENT_SOURCE_DIR}/file.cpp" 
#               "${CMAKE_CURRENT_SOURCE_DIR}/file.h")
target_link_libraries(executable_name PRIVATE library)
target_compile_features(executable_name PRIVATE cxx_std_14)
