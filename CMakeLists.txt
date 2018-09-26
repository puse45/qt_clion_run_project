cmake_minimum_required(VERSION 3.10)
project(qt_clion_run_project)
set(CMAKE_RUNTIME_OUTPUT_DIRECTORY ${CMAKE_BINARY_DIR}/../Debug)
set(EXECUTABLE_OUTPUT_PATH ${CMAKE_SOURCE_DIR}/../Release)
set(CMAKE_AUTOMOC ON)
set(CMAKE_AUTOUIC ON)
set(CMAKE_INCLUDE_CURRENT_DIR ON)
# Path to Qt CMake
set (CMAKE_PREFIX_PATH "C:/Qt5/5.11.1/msvc2017_64/lib/cmake")
find_package(Qt5Widgets)
set(CMAKE_CXX_FLAGS "${CMAKE_CXX_FLAGS} ${Qt5Widgets_EXECUTABLE_COMPILE_FLAGS}")
set(SOURCE_FILES
        main.cpp
        mainwindow.cpp
        mainwindow.ui
        )

add_executable(${PROJECT_NAME} WIN32 ${SOURCE_FILES})
target_link_libraries(${PROJECT_NAME} Qt5::Widgets)
