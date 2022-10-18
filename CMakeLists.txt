cmake_minimum_required(VERSION 3.14)

project(38_5_2_Vizivic_Html_File LANGUAGES CXX)

set(CMAKE_INCLUDE_CURRENT_DIR ON)

set(CMAKE_AUTOUIC ON)
set(CMAKE_AUTOMOC ON)
set(CMAKE_AUTORCC ON)

set(CMAKE_CXX_STANDARD 17)
set(CMAKE_CXX_STANDARD_REQUIRED ON)

find_package(QT NAMES Qt6 Qt5 REQUIRED COMPONENTS
    Core
    Widgets
)
find_package(Qt${QT_VERSION_MAJOR} REQUIRED COMPONENTS
    Core
    Widgets
    WebEngineWidgets
)

add_executable(38_5_2_Vizivic_Html_File
  main.cpp
)
target_link_libraries(38_5_2_Vizivic_Html_File
    Qt${QT_VERSION_MAJOR}::Core
    Qt${QT_VERSION_MAJOR}::Widgets
    Qt${QT_VERSION_MAJOR}::WebEngineCore
    Qt${QT_VERSION_MAJOR}::WebEngineWidgets
)

install(TARGETS 38_5_2_Vizivic_Html_File
    LIBRARY DESTINATION ${CMAKE_INSTALL_LIBDIR})
