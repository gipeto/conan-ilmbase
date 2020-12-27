PROJECT(PackageTest)
cmake_minimum_required(VERSION 3.12)

include(${CMAKE_BINARY_DIR}/conanbuildinfo.cmake)
conan_basic_setup()

find_package(IlmBase REQUIRED)

add_executable(testPackage main.cpp testMatrix.cpp)
target_link_libraries(testPackage PRIVATE IlmBase::Imath)
