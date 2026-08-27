file(GLOB SOURCES
    "${CMAKE_CURRENT_SOURCE_DIR}/src/*.s"
    "${CMAKE_CURRENT_SOURCE_DIR}/src/*.c"
)

add_library(Startup STATIC ${SOURCES})

target_include_directories(Startup PUBLIC 
    "${CMAKE_CURRENT_SOURCE_DIR}/inc"
)