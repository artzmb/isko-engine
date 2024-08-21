cmake_minimum_required(VERSION 3.28)

set(ENGINE_MODULE_NAME engine)
set(ENGINE_INCLUDE_DIR "include/${ENGINE_MODULE_NAME}")
set(ENGINE_SRC_DIR "src/${ENGINE_MODULE_NAME}")

set(ENGINE_PUBLIC_INCLUDES
    ${ENGINE_INCLUDE_DIR}/hello.hpp
)

set(ENGINE_PRIVATE_SOURCES
    ${ENGINE_SRC_DIR}/hello.cpp
)

set(ENGINE_ALL_SOURCES
    ${ENGINE_PUBLIC_INCLUDES}
    ${ENGINE_PRIVATE_SOURCES}
)

add_library(${ENGINE_MODULE_NAME}
    ${ENGINE_ALL_SOURCES}
)

source_group(TREE ${CMAKE_CURRENT_SOURCE_DIR} FILES
    ${ENGINE_ALL_SOURCES}
)

target_include_directories(${ENGINE_MODULE_NAME} PUBLIC include)
target_include_directories(${ENGINE_MODULE_NAME} PRIVATE src)
target_compile_features(${ENGINE_MODULE_NAME} PUBLIC cxx_std_17)
