cmake_minimum_required(VERSION 3.12)

project(REDasmDatabase)

if(WIN32)
    set(REDASM_DATABASE_ROOT database)
else()
    include(GNUInstallDirs)
    set(REDASM_DATABASE_ROOT ${CMAKE_INSTALL_DATADIR}/redasm/database)
endif()

# Loaders
install(DIRECTORY loaders
        DESTINATION ${REDASM_DATABASE_ROOT}
        FILES_MATCHING PATTERN "*.json")

install(DIRECTORY loaders
        DESTINATION ${REDASM_DATABASE_ROOT}
        FILES_MATCHING PATTERN "*.rdb")
