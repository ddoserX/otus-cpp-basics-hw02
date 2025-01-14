cmake_minimum_required(VERSION 3.12)

project(01.hello_world)

set(SRC_MAIN
    source/hello_world.cpp
)

set(SRC_ADDIT
    source/example.cpp
    source/example.hpp
    source/move_me_out.cpp
    source/move_me_out.hpp
)

add_executable(hello_world 
    ${SRC_ADDIT}
    ${SRC_MAIN}
)

target_compile_options(hello_world PUBLIC
    -Wall
    -Wextra
    -Werror
    -pedantic
)

set_target_properties(hello_world PROPERTIES
    CXX_STANDARD 17
    CXX_STANDARD_REQUIRED ON
)