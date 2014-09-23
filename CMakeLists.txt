cmake_minimum_required(VERSION 2.8)
project(Cmake)

find_package(Qt5Widgets)

qt5_wrap_cpp(Cmake_hdr_moc mainwindow.h)
qt5_wrap_ui(Cmake_form_hdr mainwindow.ui)

include_directories (${PROJECT_BINARY_DIR})

add_executable(Cmake main.cpp mainwindow.cpp ${Cmake_hdr_moc} ${Cmake_form_hdr})
qt5_use_modules(Cmake Core Gui Widgets)
