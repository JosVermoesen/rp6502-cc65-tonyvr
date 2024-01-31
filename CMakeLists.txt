cmake_minimum_required(VERSION 3.13)

project(MY-RP6502-PROJECT C ASM)

add_subdirectory(tools)

add_executable(bgdemo)
rp6502_executable(bgdemo)
target_sources(bgdemo PRIVATE
    src/bitmap_graphics.c
    src/main_bgdemo.c
)

add_executable(tetricks)
rp6502_executable(tetricks)
target_sources(tetricks PRIVATE
    src/main_tetricks.c
    src/bitmap_graphics.c
)
