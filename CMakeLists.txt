cmake_minimum_required(VERSION 3.7)
project(try_googletest)

include_directories(
        ${CMAKE_CURRENT_SOURCE_DIR}/deps/gtest/include
        ${CMAKE_CURRENT_SOURCE_DIR}/src
)

set(CMAKE_CXX_STANDARD 11)

set(SOURCE_FILES src/sample1.cc src/sample1_unittest.cc)
add_executable(sample1_unittest ${SOURCE_FILES})
target_link_libraries(sample1_unittest
                      ${CMAKE_CURRENT_SOURCE_DIR}/deps/gtest/lib/libgtest.a
                      ${CMAKE_CURRENT_SOURCE_DIR}/deps/gtest/lib/libgtest_main.a
                      pthread # pthread should be last because of static libraries link order
                      )

set(SOURCE_FILES src/sample2.cc src/sample2_unittest.cc)
add_executable(sample2_unittest ${SOURCE_FILES})
target_link_libraries(sample2_unittest
                      ${CMAKE_CURRENT_SOURCE_DIR}/deps/gtest/lib/libgtest.a
                      ${CMAKE_CURRENT_SOURCE_DIR}/deps/gtest/lib/libgtest_main.a
                      pthread # pthread should be last because of static libraries link order
                     )