# -- Minimum required version
cmake_minimum_required (VERSION 3.11.0)

# -- Project name
project (apue)

# -- Various includes
include (GenerateExportHeader)
include (CMakePackageConfigHelpers)
include (GNUInstallDirs)

# -- Required to build
set(CMAKE_THREAD_PREFER_PTHREAD TRUE)
set(THREADS_PREFER_PTHREAD_FLAG TRUE)
find_package(Threads REQUIRED)

# -- Set c11 standard default
set(CMAKE_C_STANDARD 11)
set(CMAKE_C_STANDARD_REQUIRED ON)

# -- Add globally compile options
add_compile_options(-Wall -Wextra -pedantic -Werror)

# -- Add Chapter 1
add_subdirectory(01)

# -- Add Chapter 2
add_subdirectory(02)
