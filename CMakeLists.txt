cmake_minimum_required(VERSION 3.13)
add_library("rtcpi" STATIC
    "src/data_socket.cc"
    "src/utils.cc"
)
target_link_directories("rtcpi" INTERFACE
    "${CMAKE_CURRENT_SOURCE_DIR}/lib"
)
target_include_directories("rtcpi" INTERFACE
    "${CMAKE_CURRENT_SOURCE_DIR}/src"
)
target_include_directories("rtcpi" PRIVATE
    "${CMAKE_CURRENT_SOURCE_DIR}/inc"
)
target_link_libraries("rtcpi" INTERFACE "webrtc")
