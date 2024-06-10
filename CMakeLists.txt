cmake_minimum_required(VERSION 3.13)
project(gtk_tutorial)

set(SOURCE_FILES main.c)

add_executable(gtk_tutorial ${SOURCE_FILES})
find_package(PkgConfig REQUIRED)
pkg_check_modules(GTK4 REQUIRED IMPORTED_TARGET gtk4)

target_link_libraries(gtk_tutorial PRIVATE PkgConfig::GTK4)
