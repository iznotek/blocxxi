# Catch2
add_subdirectory(catch2)

# Boost
set(BOOST_URL https://boostorg.jfrog.io/artifactory/main/release/1.69.0/source/boost_1_69_0.tar.bz2 CACHE STRING "Boost download URL" FORCE)
set(BOOST_URL_SHA256 8f32d4617390d1c2d16f26a27ab60d97807b35440d45891fa340fc2648b04406 CACHE STRING "Boost download URL SHA256 checksum" FORCE)
add_subdirectory(boost-cmake)

add_subdirectory(gsl-lite)
SET(SPDLOG_BUILD_TESTING OFF CACHE BOOL "Build spdlog tests")
add_subdirectory(spdlog)
add_subdirectory(miniupnpc)
add_subdirectory(imgui-cmake)
SET(GLFW_BUILD_TESTS OFF)
add_subdirectory(glfw)
SET(USE_SYSTEM_TZ_DB ON CACHE BOOL "Use system TZ db for date library" FORCE)
SET(ENABLE_DATE_TESTING OFF CACHE BOOL "Build tests for the date library" FORCE)
set(CMAKE_CXX_STANDARD 14 CACHE STRING "The C++ standard whose features are requested.")
add_subdirectory(date)
set(YAML_CPP_BUILD_TESTS OFF CACHE BOOL "Enable testing" FORCE)
set(YAML_CPP_BUILD_CONTRIB OFF CACHE BOOL "Enable contrib stuff in library")
add_subdirectory(yaml-cpp)
