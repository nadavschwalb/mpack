cmake_minimum_required(VERSION 3.15)

project(mpack)

add_library(${PROJECT_NAME} STATIC
    src/mpack/mpack-common.c
    src/mpack/mpack-expect.c
    src/mpack/mpack-node.c
    src/mpack/mpack-platform.c
    src/mpack/mpack-reader.c
    src/mpack/mpack-writer.c
)

target_include_directories(${PROJECT_NAME} PUBLIC mpack
    ${CMAKE_CURRENT_LIST_DIR}/src/mpack
)