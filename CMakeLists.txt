cmake_minimum_required(VERSION 3.8.2)
project (Inotify)

add_subdirectory (test)

add_library (Inotify INTERFACE)
target_include_directories (Inotify INTERFACE ${CMAKE_CURRENT_SOURCE_DIR}/include)
