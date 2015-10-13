add_executable (ball-in-maze tut_ball_in_maze.cpp world.cpp world.h )
#target_link_libraries(ball-in-maze -L/usr/local/lib64/panda3d p3framework panda pandafx pandaexpress p3dtoolconfig p3dtool p3direct)

set_target_properties(ball-in-maze PROPERTIES COMPILE_FLAGS -fPIC)


target_link_libraries(ball-in-maze p3util
        Panda3D::p3framework
        Panda3D::panda
        Panda3D::pandafx
        Panda3D::pandaexpress
        Panda3D::p3dtool
        Panda3D::p3dtoolconfig
        Panda3D::p3pystub
        Panda3D::p3direct
${CMAKE_THREAD_LIBS_INIT}
)


