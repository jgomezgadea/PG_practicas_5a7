cmake_minimum_required(VERSION 3.0)

project(PG)

set(CMAKE_MODULE_PATH ${CMAKE_MODULE_PATH} "${CMAKE_SOURCE_DIR}/cmake/Modules/")


if (MSVC)
 add_compile_options(/W3 /WX)
else()
 set (CMAKE_CXX_STANDARD 14)
 add_compile_options(-W -Wall)
#  set(CMAKE_CXX_FLAGS "-O2 -std=c++0x -Wall")
  set(CMAKE_CXX_FLAGS_DEBUG "${CMAKE_CXX_FLAGS_DEBUG} -Wall -D_DEBUG")
endif()










add_subdirectory(librerias/guipg) #Mandatory
add_subdirectory(PGUPV) #Mandatory
add_subdirectory(ej6-1)
add_subdirectory(ej6-2)
add_subdirectory(ej6-3)
add_subdirectory(p5)
add_subdirectory(ej5-1)
add_subdirectory(ej5-2)
