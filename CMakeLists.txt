cmake_minimum_required(VERSION 3.1)
project(game.libretro.scummvm)

list(APPEND CMAKE_MODULE_PATH ${PROJECT_SOURCE_DIR})

find_package(Kodi REQUIRED)
find_package(libretro-scummvm REQUIRED)

set(SCUMMVM_CUSTOM_BINARY ${SCUMMVM_LIB}
    ${PROJECT_NAME}${CMAKE_SHARED_LIBRARY_SUFFIX})

build_addon(${PROJECT_NAME} SCUMMVM "")
