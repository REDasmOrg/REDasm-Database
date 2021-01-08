cmake_minimum_required(VERSION 3.10)

project(REDasmDatabase)
include(GNUInstallDirs)

set(REDASM_DATABASE_ROOT ${CMAKE_INSTALL_DATADIR}/redasm/database)
 
# Loaders
install(DIRECTORY loaders
        DESTINATION ${REDASM_DATABASE_ROOT}
        FILES_MATCHING PATTERN "*.json")

install(DIRECTORY loaders
        DESTINATION ${REDASM_DATABASE_ROOT}
        FILES_MATCHING PATTERN "*.rdb")
