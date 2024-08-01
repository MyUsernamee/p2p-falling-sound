cmake_minimum_required(VERSION 3.24)
project(p2p-falling-sand)

include (FetchContent)

set(CMAKE_CXX_STANDARD 17)

FetchContent_Declare(
            raylib
            GIT_REPOSITORY https://github.com/raysan5/raylib.git
            GIT_TAG 5.0.0
    )

include_directories(src)

# sources
file(GLOB_RECURSE SOURCES src/*.cpp)

# executable
add_executable(p2p-falling-sand ${SOURCES})

# link libraries
target_link_libraries(p2p-falling-sand raylib)
