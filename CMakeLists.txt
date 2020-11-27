#This will create executables of the nodes
add_executable(demo_topic_publisher src/demo_topic_publisher.cpp)
add_executable(demo_topic_subscriber src/demo_topic_subscriber.cpp)

#This will generate message header file before building the target
add_dependencies(demo_topic_publisher MystudentID_ros_demo_pkg_generate_messages_cpp)
add_dependencies(demo_topic_subscriber MystudentID _ros_demo_pkg_generate_messages_cpp)

#This will link executables to the appropriate librariesROBOTICS EEE_7_ROB WORKSHOP MANUEL
target_link_libraries(demo_topic_publisher ${catkin_LIBRARIES})
target_link_libraries(demo_topic_subscriber ${catkin_LIBRARIES})