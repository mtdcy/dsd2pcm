cmake_minimum_required (VERSION 3.2)

project (dsd2pcm)

set (dsd_source_files 
    dsd2pcm.c
    noiseshape.c
    )

set (dsd_header_files 
    dsd2pcm.h 
    noiseshape.h
    )

add_library (dsd ${dsd_source_files})

install (TARGETS dsd DESTINATION lib)
install (FILES ${dsd_header_files} DESTINATION include/dsd2pcm)
