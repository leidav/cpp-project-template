set(CMAKE_AUTOUIC ON)
set(CMAKE_AUTOMOC ON)
set(CMAKE_INCLUDE_CURRENT_DIR ON)
find_package(Qt5 COMPONENTS Core Widgets REQUIRED)

add_executable(${PROJECT_NAME}_gui WIN32 main.cpp)
#target_sources(${PROJECT_NAME}_gui
#               "${CMAKE_CURRENT_SOURCE_DIR}/file.h"
#			   "${CMAKE_CURRENT_SOURCE_DIR}/file.cpp"
#			   "${CMAKE_CURRENT_SOURCE_DIR}/file.ui"
#			   "${CMAKE_CURRENT_SOURCE_DIR}/file.qrc")
target_link_libraries(${PROJECT_NAME}_gui )
