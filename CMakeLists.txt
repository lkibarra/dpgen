# author: Your Name
# NetID: Your NetID
# Date: 06 January 2016
# Project Number: 

# This file is an exception to the Code of Academic Integrity, and may be reused without
# the need to request permission for future assignments **as long as all edits are made by
# the submitting student**. Once a student modifies the file, they may not share it with
# any other student; sharing it in any way is a violation of the Code of Academic Integrity.

# A simple example CMake Setup for Compiling C Programs. This setup utilizes a single
# subdirectory (src) in which all C source (.c) and header (.h) files within that 
# directory are included within the project.

# CMake projects are forward compatible, but may not be backwards compatible. This
# commands defines the version of CMake used for the current setup.

cmake_minimum_required(VERSION 2.6)

# Define the project name. 
project (leslieibarra_salinas4_sfarris_dpgen)

# Add a subdirectory to the project. The CMakeLists.txt file in that subdirectory
# will be used for further setting up the project.

add_subdirectory( src )
