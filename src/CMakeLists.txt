add_executable(${PROJECT_NAME} main.cpp)
#target_sources(project_name PRIVATE 
#               "${CMAKE_CURRENT_SOURCE_DIR}/file.cpp" 
#               "${CMAKE_CURRENT_SOURCE_DIR}/file.h")
target_link_libraries(${PROJECT_NAME} library)
