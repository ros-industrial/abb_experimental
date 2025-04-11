cmake_minimum_required(VERSION 3.0.2)

project(abb_irb1300_support)

find_package(catkin REQUIRED)

catkin_package()

if (CATKIN_ENABLE_TESTING)
  find_package(roslaunch REQUIRED)
  roslaunch_add_file_check(tests/roslaunch_test_irb1300_10_115.xml)
  roslaunch_add_file_check(tests/roslaunch_test_irb1300_7_140.xml)
  roslaunch_add_file_check(tests/roslaunch_test_irb1300_12_140.xml)
endif()

foreach(dir config launch meshes urdf)
   install(DIRECTORY ${dir}/
      DESTINATION ${CATKIN_PACKAGE_SHARE_DESTINATION}/${dir})
endforeach()
