INCLUDE_DIRECTORIES(${CMAKE_CURRENT_SOURCE_DIR}/inc)
AUX_SOURCE_DIRECTORY(${CMAKE_CURRENT_SOURCE_DIR}/src SRC)
ADD_LIBRARY(log SHARED ${SRC})

SET(SRC_DEMO demo.cpp)
ADD_EXECUTABLE(Demo_log ${SRC_DEMO})
TARGET_LINK_LIBRARIES(Demo_log log)

