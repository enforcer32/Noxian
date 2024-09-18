cmake_minimum_required(VERSION 3.28)

project(Noxian
	VERSION 1.0.0
	LANGUAGES CXX
)

# CONFIGS
set(CMAKE_CXX_STANDARD 20)
set(CMAKE_CXX_STANDARD_REQUIRED ON)
set(CMAKE_CXX_EXTENSIONS OFF)

set(NXN_TARGET_NAME NXN)
set(NXNTEST_TARGET_NAME NXNTest)
set(NXNSANDBOX_TARGET_NAME NXNSandbox)

# Extensions
include(FetchContent)

FetchContent_Declare(
        googletest
        GIT_REPOSITORY "https://github.com/google/googletest"
        GIT_TAG "v1.14.0"
        GIT_SHALLOW TRUE
)
FetchContent_MakeAvailable(googletest)

add_subdirectory(${NXN_TARGET_NAME})
add_subdirectory(${NXNTEST_TARGET_NAME})
add_subdirectory(${NXNSANDBOX_TARGET_NAME})
