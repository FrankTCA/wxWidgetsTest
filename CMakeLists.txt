cmake_minimum_required(VERSION 3.17)

project("CMakeTest")

set(CMAKE_CXX_STANDARD 17)
set(CMAKE_CXX_STANDARD_REQUIRED ON)

add_subdirectory("lib/wxWidgets-3.1.4")

file(GLOB MY_SOURCES "src/*.cpp" "src/*.hpp" "src/*.h")
add_executable("${PROJECT_NAME}" ${MY_SOURCES})

target_link_libraries(${PROJECT_NAME} PUBLIC wx::net wx::core wx::base)
