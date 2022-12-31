cmake_minimum_required(VERSION 3.12)
project(CellularAutomata)

set(CMAKE_CXX_STANDARD 14)

if (APPLE)
    set(CMAKE_CXX_FLAGS "-framework Cocoa -framework IOKit")
    # -framework OpenGL -framework CoreVideo
    add_compile_definitions(GL_SILENCE_DEPRECATION)
endif ()

include_directories("/usr/local/include")
add_executable(CellularAutomata main.cpp glad.c)

target_link_libraries(CellularAutomata "/usr/local/lib/libglfw3.a")