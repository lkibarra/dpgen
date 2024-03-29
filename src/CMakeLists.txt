# Author: Roman Lysecky
# NetID: rlysecky
# Date: 06 January 2016
# Project Number: 

# This file is an exception to the Code of Academic Integrity, and may be reused without
# the need to request permission for future assignments **as long as all edits are made by
# the submitting student**. Once a student modifies the file, they may not share it with
# any other student; sharing it in any way is a violation of the Code of Academic Integrity.

# Windows does weird things sometimes. This helps control the madness.
if(MSVC)
    # Sets the compilation flags to report warnings through Level 4. We used to use "-Wall" until
    # the MSVC compiler started freaking out all the time about secure scanf, etc.
    set(CMAKE_CXX_FLAGS "-W4" )
    set(CMAKE_DEBUG_POSTFIX "d")
    add_definitions(-D_CRT_SECURE_NO_DEPRECATE)
    add_definitions(-D_CRT_NONSTDC_NO_DEPRECATE)
else()
    # adds debug information for all other OSs
    add_definitions(-Wall -g)
endif()

# The following file GLOB command will search for all files within the current directory
# that match the specified expressions (*.c and *.h), and assign the resulting files
# to the variable SRCS. Thus, SRCS is a list a all C source and header files in the 
# current directory.

file( GLOB SRCS *.cpp *.h )

# Define the target application executable (named echoer) and the list of C source
# and header files needed for the executable.

add_executable( dpgen ${SRCS} )

set(CMAKE_CXX_FLAGS "${CMAKE_CXX_FLAGS} -std=c++11")
