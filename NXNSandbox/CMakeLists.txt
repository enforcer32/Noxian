file(GLOB_RECURSE NXNSandboxSources
	"${CMAKE_CURRENT_SOURCE_DIR}/NXNSandbox.cpp"
)

add_executable(${NXNSANDBOX_TARGET_NAME} ${NXNSandboxSources})
target_include_directories(${NXNSANDBOX_TARGET_NAME} PRIVATE "${CMAKE_CURRENT_SOURCE_DIR}/../")
target_link_libraries(${NXNSANDBOX_TARGET_NAME} PRIVATE ${NXN_TARGET_NAME})
