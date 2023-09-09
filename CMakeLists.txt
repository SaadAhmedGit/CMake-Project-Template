cmake_minimum_required(VERSION 3.26)
project(template CXX)

set(CMAKE_CXX_STANDARD 17)

include_directories(include)
set_target_properties(PROPERTIES LINKER_LANGUAGE CXX)

file(GLOB LIB_SOURCES "include/*.h" "src/*.cpp")

if (LIB_SOURCES)
    add_library(headers ${LIB_SOURCES})
endif()

add_executable(main src/main.cpp)

if (LIB_SOURCES)
    target_link_libraries(main headers)
endif()

set(CMAKE_CXX_FLAGS_DEBUG "${CMAKE_CXX_FLAGS_DEBUG} -O0 -fdiagnostics-color=always -fsanitize=address -DLOCAL_ENV -fno-omit-frame-pointer -fno-inline -g3")
set(CMAKE_CXX_FLAGS_RELEASE "${CMAKE_CXX_FLAGS_RELEASE} -O3 -fdiagnostics-color=always -ffunction-sections -fdata-sections -DNDEBUG -Wall")
