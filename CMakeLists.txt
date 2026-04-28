cmake_minimum_required(VERSION 3.10)
project(my_project)

set(CMAKE_CXX_STANDARD 17)
set(CMAKE_CXX_STANDARD_REQUIRED ON)

find_package(GTest REQUIRED)

enable_testing()

add_executable(prime_test  test.cpp UserRegistration.cpp EmailService.hpp  UserRegistration.hpp)
target_link_libraries(prime_test PRIVATE GTest::gtest GTest::gmock_main)
include(GoogleTest)
gtest_discover_tests(prime_test)
