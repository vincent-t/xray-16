cmake_minimum_required(VERSION 2.8.0)
project(OpenXRay)

set(CMAKE_MODULE_PATH ${PROJECT_SOURCE_DIR}/cmake)

set(CMAKE_CXX_FLAGS "${CMAKE_CXX_FLAGS} -fpermissive --std=c++11")

add_definitions(-D_MT -D_CPPUNWIND -DPURE_DYNAMIC_CAST -DDECLARE_SPECIALIZATION -DM_NOSTDCONTAINERS_EXT -DUSE_OGL)

find_package(Lua51 REQUIRED)
find_package(OpenSSL REQUIRED)
find_package(Theora REQUIRED)
find_package(OGG REQUIRED)
find_package(SDL2 REQUIRED)
find_package(LZO REQUIRED)

include_directories(${LUA_INCLUDE_DIR})
include_directories(${CMAKE_SOURCE_DIR} {CMAKE_SOURCE_DIR}/Common ${CMAKE_SOURCE_DIR}/Externals ${CMAKE_SOURCE_DIR}/Externals/gli/external/glm ${CMAKE_SOURCE_DIR}/../sdk/include/loki)

#add_subdirectory(utils)
add_subdirectory(Externals)
#add_subdirectory(Layers)
#add_subdirectory(xrMisc)
#add_subdirectory(xrAICore)
#add_subdirectory(xrCDB)
add_subdirectory(xrCore)
#add_subdirectory(xrEngine)
#add_subdirectory(xrGame)
#add_subdirectory(xrNetServer)
#add_subdirectory(xrParticles)
#add_subdirectory(xrPhysics)
#add_subdirectory(xrScriptEngine)
#add_subdirectory(xrSound)
