cmake_minimum_required(VERSION 2.4.6)
include($ENV{ROS_ROOT}/core/rosbuild/rosbuild.cmake)

# Set the build type.  Options are:
#  Coverage       : w/ debug symbols, w/o optimization, w/ code-coverage
#  Debug          : w/ debug symbols, w/o optimization
#  Release        : w/o debug symbols, w/ optimization
#  RelWithDebInfo : w/ debug symbols, w/ optimization
#  MinSizeRel     : w/o debug symbols, w/ optimization, stripped binaries
#set(ROS_BUILD_TYPE RelWithDebInfo)

rosbuild_init()

#set the default path for built executables to the "bin" directory
set(EXECUTABLE_OUTPUT_PATH ${PROJECT_SOURCE_DIR}/bin)
#set the default path for built libraries to the "lib" directory
set(LIBRARY_OUTPUT_PATH ${PROJECT_SOURCE_DIR}/lib)
#uncomment if you have defined messages
#rosbuild_genmsg()
#uncomment if you have defined services
#rosbuild_gensrv()

#common commands for building c++ executables and libraries
#rosbuild_add_library(${PROJECT_NAME} src/example.cpp)
#target_link_libraries(${PROJECT_NAME} another_library)
#rosbuild_add_boost_directories()
#rosbuild_link_boost(${PROJECT_NAME} thread)
#rosbuild_add_executable(example examples/example.cpp)
#target_link_libraries(example ${PROJECT_NAME})

#-------------------------------------------------------------
#  executables binary
#-------------------------------------------------------------
#rosbuild_add_executable(labelViwer src/test/label_viwer.cpp)
#rosbuild_add_executable(eyeOfGraeae src/graeae.cpp)

#-------------------------------------------------------------
#  TEST : executables binary
#-------------------------------------------------------------
rosbuild_add_executable(segmenter src/test/segmenter_test.cpp)
rosbuild_add_executable(colorMapping src/colorMapping.cpp)
#rosbuild_add_executable(pulish_pc_demo src/test/pulish_pc_demo.cpp)
#rosbuild_add_executable(labeller src/test/labeller.cpp)

#-------------------------------------------------------------
#  link libraries
#-------------------------------------------------------------
#target_link_libraries(labelViwer vtkCommon vtkFiltering)
#target_link_libraries(eyeOfGraeae vtkCommon vtkFiltering)
#target_link_libraries(labeller vtkCommon vtkFiltering vtkRendering)
