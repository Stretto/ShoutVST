project (ShoutVST)

set (CMAKE_CXX_STANDARD 11)
set(CMAKE_CXX_STANDARD_REQUIRED ON)

set(LIBRARY_OUTPUT_PATH "${CMAKE_CURRENT_SOURCE_DIR}/../ShoutVST_DLL")

include_directories (${CMAKE_CURRENT_SOURCE_DIR}/..)

aux_source_directory(${CMAKE_CURRENT_SOURCE_DIR}/../ SOURCES)

add_library(${PROJECT_NAME}  SHARED ${SOURCES})

TARGET_LINK_LIBRARIES(${PROJECT_NAME} VST_SDK shout ogg vorbis mp3lame fluid-gui)
