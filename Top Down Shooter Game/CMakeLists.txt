cmake_minimum_required(VERSION 3.10)

# Set raylib installation path
set(CMAKE_PREFIX_PATH "C:/raylib" ${CMAKE_PREFIX_PATH})

include_directories("C:/raylib/raylib/src")
link_directories("C:/raylib/raylib/src")

file(GLOB SOURCES "*.cpp")

add_executable(${PROJECT_NAME} ${SOURCES})

target_link_libraries(${PROJECT_NAME} raylib winmm)

target_include_directories(${PROJECT_NAME} PRIVATE .)