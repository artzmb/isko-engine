cmake_minimum_required(VERSION 3.28)

set(EDITOR_MODULE_NAME editor)

add_executable(${EDITOR_MODULE_NAME}
    src/main.cpp
)

target_link_libraries(${EDITOR_MODULE_NAME} engine)
target_compile_features(${EDITOR_MODULE_NAME} PUBLIC cxx_std_17)

set_target_properties(${EDITOR_MODULE_NAME} PROPERTIES RUNTIME_OUTPUT_DIRECTORY ${CMAKE_BINARY_DIR}/bin/)
