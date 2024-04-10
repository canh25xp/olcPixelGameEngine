add_library(olcPixelGameEngine olcExampleProgram.cpp)

target_include_directories(olcPixelGameEngine
                           INTERFACE
                           $<BUILD_INTERFACE:${CMAKE_CURRENT_SOURCE_DIR}>
                           $<INSTALL_INTERFACE:include>
                           )

target_link_libraries(olcPixelGameEngine PRIVATE compiler_flags X11 GL pthread png stdc++fs)
