cmake_minimum_required(VERSION 3.15)
project(mosquitto_project CXX)

find_package(mosquitto)

add_executable(${PROJECT_NAME} src/mqtt_pub.cpp)

# Use the global target
target_link_libraries(${PROJECT_NAME} mosquitto::mosquitto)

