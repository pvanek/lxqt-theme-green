cmake_minimum_required(VERSION 2.8.11)

project(lxqt-theme-green)

find_package(lxqt REQUIRED)
include(${LXQT_USE_FILE})

install(DIRECTORY Green DESTINATION share/lxqt/themes PATTERN "CMake*" EXCLUDE PATTERN "cmake*" EXCLUDE PATTERN "Makefile" EXCLUDE)

# building tarball with CPack -------------------------------------------------
include(InstallRequiredSystemLibraries)
set(CPACK_PACKAGE_VERSION_MAJOR ${LXQT_MAJOR_VERSION})
set(CPACK_PACKAGE_VERSION_MINOR ${LXQT_MINOR_VERSION})
set(CPACK_PACKAGE_VERSION_PATCH ${LXQT_PATCH_VERSION})
set(CPACK_GENERATOR TBZ2)
set(CPACK_SOURCE_GENERATOR TBZ2)
set(CPACK_SOURCE_IGNORE_FILES /build/;.gitignore;.*~;.git;.kdev4;temp)
include(CPack)
