add_executable(gym_client gym_client.cpp communicator.cpp)

target_include_directories(gym_client 
    PRIVATE
    .
    ../include
    ../deps
    ../deps/lib/spdlog/include
    ../deps/lib/msgpack-c/include
    ../deps/lib/spdlog/include
    ../deps/lib/libzmq/include
)

target_link_libraries(gym_client PRIVATE libzmq-static cpprl)