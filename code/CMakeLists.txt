cmake_minimum_required(VERSION 2.8.3)
project(project2)

find_package(catkin REQUIRED COMPONENTS roslaunch)

catkin_package()

roslaunch_add_file_check(launch/include/amcl.launch)
roslaunch_add_file_check(launch/include/gmapping.launch)
roslaunch_add_file_check(launch/include/imu_filter.launch)
roslaunch_add_file_check(launch/amcl_test.launch)
roslaunch_add_file_check(launch/opti_gmapping.launch)
roslaunch_add_file_check(launch/cam_gmapping.launch)
roslaunch_add_file_check(launch/ekf_localization.launch)


install(
DIRECTORY launch maps params
DESTINATION ${CATKIN_PACKAGE_SHARE_DESTINATION}
)
