# Generated Cmake Pico project file

cmake_minimum_required(VERSION 3.13)

set(CMAKE_C_STANDARD 11)
set(CMAKE_CXX_STANDARD 17)

# Pull in Raspberry Pi Pico SDK (must be before project)
include(pico_sdk_import.cmake)

project(pico-led-ext-nn C CXX ASM)

# Initialise the Raspberry Pi Pico SDK
pico_sdk_init()

# Add executable. Default name is the project name, version 0.1

add_executable(pico-led-ext-nn pico-led-ext-nn.c )

pico_set_program_name(pico-led-ext-nn "pico-led-ext-nn")
pico_set_program_version(pico-led-ext-nn "0.1")

pico_enable_stdio_uart(pico-led-ext-nn 0)
pico_enable_stdio_usb(pico-led-ext-nn 1)

# Add the standard library to the build
target_link_libraries(pico-led-ext-nn pico_stdlib)

pico_add_extra_outputs(pico-led-ext-nn)

