cmake_minimum_required (VERSION 3.10)
set(CMAKE_CXX_STANDARD 17)
set(CMAKE_CXX_STANDARD_REQUIRED ON)
project (client LANGUAGES CXX)

find_package(Boost 1.80.0 COMPONENTS iostreams filesystem ) 

if(Boost_FOUND)
    include_directories(${Boost_INCLUDE_DIRS}) 
    add_executable(client client.cpp) 
    target_link_libraries(client ${Boost_LIBRARIES})
endif()


