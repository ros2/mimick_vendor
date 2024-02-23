cmake_minimum_required(VERSION 3.10)
project(mimick_vendor)

find_package(ament_cmake REQUIRED)
find_package(ament_cmake_vendor_package REQUIRED)

ament_vendor(mimick_vendor
  VCS_URL https://github.com/christophebedard/Mimick.git
  VCS_VERSION 55500d640683f44de12a8211531395a8b8198292
)

ament_export_dependencies(mimick)

if(BUILD_TESTING)
  find_package(ament_lint_auto REQUIRED)
  ament_lint_auto_find_test_dependencies()
endif()

ament_package()
