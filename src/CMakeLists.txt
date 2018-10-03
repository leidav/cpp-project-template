add_executable(${PROJECT_NAME} main.cpp)
#target_sources(project_name PRIVATE 
#               "${CMAKE_CURRENT_SOURCE_DIR}/file.cpp" 
#               "${CMAKE_CURRENT_SOURCE_DIR}/file.h")
target_link_libraries(${PROJECT_NAME} PRIVATE library)
target_compile_features(${PROJECT_NAME} PRIVATE cxx_std_14)
