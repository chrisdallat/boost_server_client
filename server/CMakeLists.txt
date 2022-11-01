cmake_minimum_required (VERSION 3.10)
set(CMAKE_CXX_STANDARD 17)
set(CMAKE_CXX_STANDARD_REQUIRED ON)
project (server LANGUAGES CXX)

find_package(Boost 1.80.0 COMPONENTS iostreams filesystem ) 

if(Boost_FOUND)
    include_directories(${Boost_INCLUDE_DIRS}) 
    add_executable(server server.cpp) 
    target_link_libraries(server ${Boost_LIBRARIES})
endif()


