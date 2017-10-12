set(CMAKE_AUTOUIC ON)
set(CMAKE_AUTOMOC ON)
set(CMAKE_INCLUDE_CURRENT_DIR ON)
find_package(Qt5 COMPONENTS Core Widgets REQUIRED)

add_executable(${PROJECT_NAME}_gui WIN32 main.cpp)
#add_sources(file.h file.cpp file.ui file.qrc)
target_link_libraries(${PROJECT_NAME}_gui )
