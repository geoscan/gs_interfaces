cmake_minimum_required(VERSION 2.8.3)
project(gs_interfaces)

find_package(catkin REQUIRED
    COMPONENTS message_generation std_msgs geometry_msgs sensor_msgs
)

add_message_files(
   FILES
   PointGPS.msg
   SimpleBatteryState.msg
   OptVelocity.msg
   Orientation.msg
   SatellitesGPS.msg
   Parameter.msg
)

add_service_files(
   FILES
   Yaw.srv
   Event.srv
   Led.srv
   Time.srv
   Info.srv
   Live.srv
   Log.srv
   NavigationSystem.srv
   SetNavigationSystem.srv
   Position.srv
   PositionGPS.srv
   ParametersList.srv
   SetParametersList.srv
)

generate_messages(
   DEPENDENCIES std_msgs geometry_msgs sensor_msgs gs_interfaces
)

catkin_package(
   CATKIN_DEPENDS message_runtime
)

include_directories()
