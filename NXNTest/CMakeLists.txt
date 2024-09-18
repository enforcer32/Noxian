file(GLOB_RECURSE NXNTestSources
	"${CMAKE_CURRENT_SOURCE_DIR}/Test.cpp"
)

add_executable(${NXNTEST_TARGET_NAME} ${NXNTestSources})
target_include_directories(${NXNTEST_TARGET_NAME} PRIVATE "${CMAKE_CURRENT_SOURCE_DIR}/../")
target_link_libraries(${NXNTEST_TARGET_NAME} PRIVATE ${NXN_TARGET_NAME})
target_link_libraries(${NXNTEST_TARGET_NAME} PRIVATE GTest::gtest_main)
