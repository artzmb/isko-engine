cmake_minimum_required(VERSION 3.28)

set(PROJECT_NAME isko-engine)
project(${PROJECT_NAME})

set(EDITOR_MODULE_NAME editor)
set(ENGINE_MODULE_NAME engine)

add_subdirectory(${EDITOR_MODULE_NAME})
add_subdirectory(${ENGINE_MODULE_NAME})

set_property(DIRECTORY ${CMAKE_CURRENT_SOURCE_DIR} PROPERTY VS_STARTUP_PROJECT ${EDITOR_MODULE_NAME})
