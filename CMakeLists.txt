cmake_minimum_required(VERSION 2.8)
project(qt4-test)
set(sources main.cpp
	MainWindow.cpp)
set(header MainWindow.h)
set(CMAKE_BUILD_TYPE Release)
set(CMAKE_AUTOMOC ON)
set(CMAKE_INCLUDE_CURRENT_DIR ON)
find_package(Qt4 4.8.6 REQUIRED QtGui QtXml)
add_executable(myexe ${sources})
target_link_libraries(myexe Qt4::QtGui Qt4::QtXml winmm imm32 ws2_32)

