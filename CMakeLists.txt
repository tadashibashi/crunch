cmake_minimum_required(VERSION 3.20)
project(crunch)

set(CMAKE_CXX_STANDARD 14)
set(CMAKE_CXX_STANDARD_REQUIRED ON)

add_library(libcrunch
    crunch/binary.cpp
    crunch/binary.hpp
    crunch/bitmap.cpp
    crunch/bitmap.hpp
    crunch/GuillotineBinPack.cpp
    crunch/GuillotineBinPack.h
    crunch/hash.cpp
    crunch/hash.hpp
    crunch/lodepng.cpp
    crunch/lodepng.h
    crunch/MaxRectsBinPack.cpp
    crunch/MaxRectsBinPack.h
    crunch/packer.cpp
    crunch/packer.hpp
    crunch/Rect.cpp
    crunch/Rect.h
    crunch/str.cpp
    crunch/str.hpp
    crunch/tinydir.h
)
target_include_directories(libcrunch "${CMAKE_CURRENT_SOURCE_DIR}")

add_executable(crunch crunch/main.cpp)
