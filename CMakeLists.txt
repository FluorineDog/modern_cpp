project(modern_cpp)
cmake_minimum_required(VERSION 3.15)
enable_testing()
#include(GoogleTest)
find_package(GTest)
# mark_as_advanced(
#     BUILD_GMOCK BUILD_GTEST BUILD_SHARED_LIBS
#     gmock_build_tests gtest_build_samples gtest_build_tests
#     gtest_disable_pthreads gtest_force_shared_crt gtest_hide_internal_symbols
# )
# set_target_properties(gtest PROPERTIES FOLDER extern)
# set_target_properties(gtest_main PROPERTIES FOLDER extern)
# set_target_properties(gmock PROPERTIES FOLDER extern)
# set_target_properties(gmock_main PROPERTIES FOLDER extern)

add_executable(main main.cpp)
target_link_libraries(main GTest::Main)
gtest_discover_tests(main)
