
add_executable(server_multithread server.cpp)
target_include_directories(server_multithread PRIVATE ${PROJECT_BINARY_DIR}/src/proto)
target_link_libraries(server_multithread PRIVATE cppzmq command_msg)

add_executable(client_multithread client.cpp)
target_include_directories(client_multithread PRIVATE ${PROJECT_BINARY_DIR}/src/proto)
target_link_libraries(client_multithread PRIVATE cppzmq command_msg)