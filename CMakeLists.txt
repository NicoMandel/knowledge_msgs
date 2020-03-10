cmake_minimum_required(VERSION 2.8.3)
project(knowledge_msgs)

find_package(catkin REQUIRED COMPONENTS
  std_msgs
  message_generation
  geometry_msgs
  sensor_msgs
)


## Generate messages in the 'msg' folder
add_message_files(
  FILES
  Object.msg
  KnownObjects.msg
  Point2D.msg
  Point2DStamped.msg
  PointArray.msg
  PathNode.msg
  Array.msg
  Dataframe.msg
  ObjectLocation.msg
  ObjectLocationList.msg
)

## Generate services in the 'srv' folder
add_service_files(
  FILES
  GetName.srv
  RegisterObject.srv
  GetDistance.srv
  GetHolonyms.srv
  GetLowestHyper.srv
  GetMeronyms.srv
  GetConnecting.srv
  GetLexname.srv
  GetIDs.srv
)


## Generate added messages and services with any dependencies listed here
generate_messages(
  DEPENDENCIES
  std_msgs
  geometry_msgs
)


catkin_package(
 CATKIN_DEPENDS std_msgs message_runtime geometry_msgs
)

include_directories(
# include
  ${catkin_INCLUDE_DIRS}
)
