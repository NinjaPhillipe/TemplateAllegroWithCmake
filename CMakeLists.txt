cmake_minimum_required(VERSION 3.0)

set(projectName InsertProjectNameHere)

project(${projectName})

set(SRCS 
    # Insert all source file    
    Src/main.cpp
)

set(HEADERS
    # Insert all headers file    
)

INCLUDE_DIRECTORIES(/usr/include/allegro5)
include_directories(Headers)
LINK_DIRECTORIES( /usr/lib )


add_executable(${projectName} ${SRCS} ${HEADERS})

TARGET_INCLUDE_DIRECTORIES(${projectName} PUBLIC  ${HEADERS})
TARGET_LINK_LIBRARIES(${projectName} allegro
        allegro_color
        allegro_main
        allegro_primitives
        allegro_ttf
        allegro_acodec
        allegro_audio
        allegro_font)
