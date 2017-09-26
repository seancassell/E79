# TEMPLATE SOURCE: https://github.com/bast/cmake-example/blob/master/CMakeLists.txt

# Stop if cmake version below 3.5:
cmake_minimum_required(VERSION 3.5 FATAL_ERROR)

# Detect host processor:
message(STATUS "The host processor is ${CMAKE_HOST_SYSTEM_PROCESSOR}")

# Project name:
project (CppWeeklyEp78)

# Enable C++:
#enable_language(Fortran C CXX)
enable_language(CXX)

# Require C++14:
set(CMAKE_CXX_STANDARD 14)

# Enable compiler-specific features:
if (MSVC)
	add_compile_options(/W4 /GA /Bv /J)
else()
	add_compile_options(-Wall -Wextra -Wpedantic)
endif()

# Set project version:
set(VERSION_MAJOR 1)
set(VERSION_MINOR 0)
set(VERSION_PATCH 1)


# Compile main executable:
add_executable(CppWeeklyEp78 cmake_intro.cpp)

