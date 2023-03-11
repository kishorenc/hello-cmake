cmake_minimum_required(VERSION 3.5)

project (hello)
add_executable(hellobin main.cpp)
add_library(hello STATIC main.cpp)

set_target_properties(hellobin PROPERTIES OUTPUT_NAME hello)
set_target_properties(hello PROPERTIES OUTPUT_NAME hello)

set(LIBRARY_OUTPUT_PATH ${PROJECT_BINARY_DIR}/lib)
install(TARGETS hello ARCHIVE DESTINATION lib)

