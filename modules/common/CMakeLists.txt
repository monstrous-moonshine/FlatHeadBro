cmake_minimum_required(VERSION 3.10)

include(${CMAKE_CURRENT_LIST_DIR}/../module.cmake)
include_guard(GLOBAL)

project(common)

enable_language( C CXX ASM )
set(CMAKE_EXPORT_COMPILE_COMMANDS ON)
set(TARGET common)
set(common_INCLUDE_DIRS 
    "${CMAKE_CURRENT_LIST_DIR}/include"
)


add_library(${TARGET} 
    "${CMAKE_CURRENT_LIST_DIR}/src/common.c" 
)

# set_target_properties(${TARGET}  PROPERTIES PREFIX "")
# set_target_properties(${TARGET}  PROPERTIES OUTPUT_NAME ${TARGET})
# set_target_properties(${TARGET}  PROPERTIES SUFFIX ".a")


target_include_directories(${TARGET} PUBLIC 
    ${common_INCLUDE_DIRS}
)



