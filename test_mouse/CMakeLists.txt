add_executable (test_mouse test_mouse.cpp )
#target_link_libraries(ball-in-maze -L/usr/local/lib64/panda3d p3framework panda pandafx pandaexpress p3dtoolconfig p3dtool p3direct)

set_target_properties(test_mouse PROPERTIES COMPILE_FLAGS -fPIC)


target_link_libraries(test_mouse p3util
        Panda3D::p3framework
        Panda3D::panda
        Panda3D::pandafx
        Panda3D::pandaexpress
        Panda3D::p3dtoolconfig
        Panda3D::p3dtool
        Panda3D::p3pystub
        Panda3D::p3direct
${CMAKE_THREAD_LIBS_INIT}
)


