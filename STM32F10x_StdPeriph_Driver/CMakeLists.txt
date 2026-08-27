file(GLOB SOURCES
    "${CMAKE_CURRENT_SOURCE_DIR}/src/*.s"
    "${CMAKE_CURRENT_SOURCE_DIR}/src/*.c"
)

add_library(STM32F10x_StdPeriph_Driver STATIC ${SOURCES})

target_include_directories(STM32F10x_StdPeriph_Driver PUBLIC 
    ${CMAKE_CURRENT_SOURCE_DIR}/inc
    $<TARGET_PROPERTY:CMSIS,INTERFACE_INCLUDE_DIRECTORIES>
)