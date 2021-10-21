add_executable(proxy proxy.cpp)
target_include_directories(proxy PRIVATE ${PROJECT_BINARY_DIR}/src/proto)
target_link_libraries(proxy PRIVATE cppzmq command_msg)

add_executable(server_load_balance server.cpp)
target_include_directories(server_load_balance PRIVATE ${PROJECT_BINARY_DIR}/src/proto)
target_link_libraries(server_load_balance PRIVATE cppzmq command_msg)

add_executable(client_load_balance client.cpp)
target_include_directories(client_load_balance PRIVATE ${PROJECT_BINARY_DIR}/src/proto)
target_link_libraries(client_load_balance PRIVATE cppzmq command_msg)