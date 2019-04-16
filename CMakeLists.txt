cmake_minimum_required(VERSION 3.10 FATAL_ERROR)
project(builder VERSION 0.1.0 LANGUAGES CXX)

add_library(flat_hash_map INTERFACE)

target_include_directories(flat_hash_map
        INTERFACE
            flat_hash_map
        )

install(TARGETS flat_hash_map
        EXPORT flat_hash_mapTargets
        LIBRARY DESTINATION ${CMAKE_INSTALL_LIBDIR}
        ARCHIVE DESTINATION ${CMAKE_INSTALL_LIBDIR}
        RUNTIME DESTINATION ${CMAKE_INSTALL_BINDIR}
        INCLUDES DESTINATION ${CMAKE_INSTALL_INCLUDEDIR})

export(TARGETS flat_hash_map
        FILE ${CMAKE_BINARY_DIR}/skarupkeConfig.cmake)

export(PACKAGE skarupke)