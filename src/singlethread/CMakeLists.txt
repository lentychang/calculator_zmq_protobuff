
add_executable(server_singlethread server.cpp)
target_include_directories(server_singlethread PRIVATE ${PROJECT_BINARY_DIR}/src/proto)
target_link_libraries(server_singlethread PRIVATE cppzmq command_msg)

add_executable(client_singlethread client.cpp)
target_include_directories(client_singlethread PRIVATE ${PROJECT_BINARY_DIR}/src/proto)
target_link_libraries(client_singlethread PRIVATE cppzmq command_msg)