cmake_minimum_required(VERSION 3.5)

project(print_ip)

set(PATCH_VERSION "1" CACHE INTERNAL "Patch version")
set(PROJECT_VESRION 0.0.${PATCH_VERSION})
project(print_ip VERSION ${PROJECT_VESRION})

add_executable(print_ip main.cpp)
set_target_properties(print_ip PROPERTIES CXX_STANDARD 17 CXX_STANDARD_REQUIRED ON)

set(CPACK_GENERATOR DEB)
set(CPACK_PACKAGE_VERSION_MAJOR "${PROJECT_VERSION_MAJOR}")
set(CPACK_PACKAGE_VERSION_MINOR "${PROJECT_VERSION_MINOR}")
set(CPACK_PACKAGE_VERSION_PATCH "${PROJECT_VERSION_PATCH}")
set(CPACK_PACKAGE_CONTACT example@example.com)

include(CPack)