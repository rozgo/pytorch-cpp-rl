add_executable(env_server env_server.cpp communicator.cpp)

target_include_directories(env_server 
PRIVATE
.
../include
../deps
../deps/lib/spdlog/include
../deps/lib/msgpack-c/include
../deps/lib/spdlog/include
../deps/lib/libzmq/include
)

target_link_libraries(env_server PRIVATE libzmq-static cpprl)