protobuf_generate_cpp(PROTO_SRCS PROTO_HDRS command_msg.proto)
add_library(command_msg "${PROTO_SRCS}" "${PROTO_HDRS}")
target_link_libraries(command_msg PUBLIC protobuf)