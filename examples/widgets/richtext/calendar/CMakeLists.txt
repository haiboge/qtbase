# Generated from calendar.pro.

cmake_minimum_required(VERSION 3.14)
project(calendar LANGUAGES CXX)

set(CMAKE_INCLUDE_CURRENT_DIR ON)

set(CMAKE_AUTOMOC ON)
set(CMAKE_AUTORCC ON)
set(CMAKE_AUTOUIC ON)

set(INSTALL_EXAMPLEDIR "examples/widgets/richtext/calendar")

find_package(Qt6 COMPONENTS Core)
find_package(Qt6 COMPONENTS Gui)
find_package(Qt6 COMPONENTS Widgets)

add_qt_gui_executable(calendar
    main.cpp
    mainwindow.cpp mainwindow.h
)
target_link_libraries(calendar PUBLIC
    Qt::Core
    Qt::Gui
    Qt::Widgets
)

install(TARGETS calendar
    RUNTIME DESTINATION "${INSTALL_EXAMPLEDIR}"
    BUNDLE DESTINATION "${INSTALL_EXAMPLEDIR}"
    LIBRARY DESTINATION "${INSTALL_EXAMPLEDIR}"
)
