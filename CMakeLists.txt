cmake_minimum_required(VERSION 3.10)

# set the project name
project(ProjectName VERSION 0.0)

include_directories(${PROJECT_SOURCE_DIR}/include)

file(GLOB sources ${PROJECT_SOURCE_DIR}/src/*.cc)
file(GLOB headers ${PROJECT_SOURCE_DIR}/include/*.hh)

# add the executable
add_executable(ProjectName Main.cc ${sources} ${headers})
target_link_libraries(ProjectName)
target_compile_options(ProjectName PRIVATE -pedantic -Wall -Wextra -Wshadow -Wconversion -Wunreachable-code -O3) # -Werror
