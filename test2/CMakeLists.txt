cmake_minimum_required(VERSION 3.20)

project (
  mainwindow
  LANGUAGES CXX
)

# Automatically add the current source and build directories to the include path.
set(CMAKE_INCLUDE_CURRENT_DIR ON)

set(CMAKE_AUTOMOC ON)    # Whether to handle moc automatically for Qt targets.
set(CMAKE_AUTORCC ON)    # Whether to handle rcc automatically for Qt targets.
set(CMAKE_AUTOUIC ON)    # Whether to handle uic automatically for Qt targets.

find_package(Qt5 COMPONENTS Core Gui Widgets)

add_executable(mainwindow WIN32
  colorswatch.cpp colorswatch.h
  main.cpp
  mainwindow.cpp mainwindow.h
  toolbar.cpp toolbar.h
)

target_link_libraries(mainwindow PUBLIC
  Qt5::Core
  Qt5::Gui
  Qt5::Widgets
)
