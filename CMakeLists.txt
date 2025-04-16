cmake_minimum_required(VERSION 3.28)
project(StarterProject)

add_executable(StarterProject)
set_property(TARGET StarterProject PROPERTY C_STANDARD 90)
set_property(TARGET StarterProject PROPERTY C_STANDARD_REQUIRED ON)

set(include_dir "${CMAKE_SOURCE_DIR}/include")
set(src_dir "${CMAKE_SOURCE_DIR}/src")

set(headers
  "${include_dir}/functions.h"
)

set(sources
  "${src_dir}/functions.c"
  "${src_dir}/main.c"
)

target_include_directories(StarterProject PRIVATE ${include_dir})
target_sources(StarterProject PRIVATE ${headers} ${sources})
source_group("Header Files" ${headers})
source_group("Source Files" ${sources})
