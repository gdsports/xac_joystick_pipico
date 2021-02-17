cmake_minimum_required(VERSION 3.13)
include(pico_sdk_import.cmake)
project(xac_joystick_pipico)
pico_sdk_init()
add_executable(xac_joystick
  xac_joystick.c
  usb_descriptors.c
)
pico_enable_stdio_uart(xac_joystick 1)
pico_add_extra_outputs(xac_joystick)

target_include_directories(xac_joystick PRIVATE ${CMAKE_CURRENT_LIST_DIR})

target_link_libraries(xac_joystick PRIVATE pico_stdlib tinyusb_device tinyusb_board)
