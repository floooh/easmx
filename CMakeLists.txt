cmake_minimum_required(VERSION 3.5)
project(easmx)
# set(CMAKE_C_STANDARD 11)

add_executable(asmx
    src/asm1802.c
    src/asm6502.c
    src/asm6805.c
    src/asm6809.c
    src/asm68hc11.c
    src/asm68hc16.c
    src/asm68k.c
    src/asm8048.c
    src/asm8051.c
    src/asm8085.c
    src/asmarm.c
    src/asmf8.c
    src/asmjag.c
    src/asmthumb.c
    src/asmx.c
    src/asmz80.c
)
target_compile_definitions(asmx PUBLIC VERSION="2.0b5")
if(MSVC)
  target_compile_options(asmx PRIVATE /W4 /WX)
else()
  target_compile_options(asmx PRIVATE -Wall -Wextra -Wno-sign-compare -Wno-unused-value -Wno-unused-but-set-variable -Wno-unused-parameter)
endif()
