cmake_minimum_required (VERSION 2.8.11)
project (Panda3d_examples)

set(CMAKE_MODULE_PATH ${PROJECT_SOURCE_DIR}/cmake)


FIND_PACKAGE (PythonLibs 2.7 REQUIRED)
IF (PYTHONLIBS_FOUND)
  include_directories(${PYTHON_INCLUDE_DIRS})
 #target_link_libraries (OFW ${PYTHON_LIBRARIES})
ENDIF (PYTHONLIBS_FOUND)

find_package(Eigen3 REQUIRED)
include_directories(${EIGEN3_INCLUDE_DIR})

#include_directories( ${ZLIB_INCLUDE_DIRS} )
#FIND_PACKAGE (ZLIB REQUIRED)
FIND_PACKAGE (Threads)

# Find the Panda3D modules
find_package(Panda3D REQUIRED)


#IF (UNIX)
#  FIND_PATH (PANDA3D_INCLUDE_DIR NAMES pandaFramework.h pandaSystem.h PATHS /usr/include/panda3d)
#  IF (PANDA3D_INCLUDE_DIR)
#    include_directories(${PANDA3D_INCLUDE_DIR})
#  ENDIF (PANDA3D_INCLUDE_DIR)
#  #target_link_libraries(OFW -L/usr/local/lib64/panda3d p3framework panda pandafx pandaexpress p3dtoolconfig p3dtool p3direct)
#ENDIF ()

#target_include_directories (Panda3d_examples p3util)

include_directories(${PROJECT_SOURCE_DIR}/p3util)
include_directories(${PROJECT_BINARY_DIR}/include)

add_library (p3util
   # p3util/cActor.cpp
   # p3util/cActorInterval.cpp
#    p3util/cBufferViewer.cpp
#    p3util/cCommonFilters.cpp
#    p3util/cFilterManager.cpp
    p3util/cOnscreenText.cpp
#    p3util/cSoundInterval.cpp
#    p3util/genericFunctionInterval.cpp
#    p3util/sleepWhenMinimized.cpp
#    p3util/cActor.h
#    p3util/cActorInterval.h
#    p3util/callbackUtil.h
#    p3util/cBufferViewer.h
#    p3util/cCommonFilters.h
#    p3util/cFilterManager.h
#    p3util/cLerpFunctionInterval.h
    p3util/cOnscreenText.h
#    p3util/cSoundInterval.h
#    p3util/genericFunctionInterval.h
#    p3util/sleepWhenMinimized.h
)



#target_include_directories (p3util ${CMAKE_CURRENT_SOURCE_DIR}/p3util)


add_subdirectory (ball_in_maze)

add_subdirectory (test_mouse)


