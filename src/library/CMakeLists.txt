add_library(library lib.cpp)
target_sources(library PUBLIC "${CMAKE_CURRENT_SOURCE_DIR}/lib.h")
target_include_directories(library PUBLIC "${CMAKE_CURRENT_SOURCE_DIR}")
