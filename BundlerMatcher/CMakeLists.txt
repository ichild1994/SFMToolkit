find_package(SiftGPU REQUIRED)
find_package(DevIL REQUIRED)
find_package(OpenGL REQUIRED)
find_package(GLUT REQUIRED)
find_package(Glew REQUIRED)

include_directories( "include/" ${SIFTGPU_INCLUDE_DIRS} ${IL_INCLUDE_DIR})

ADD_EXECUTABLE(BundlerMatcher src/main.cpp src/BundlerMatcher.cpp)

TARGET_LINK_LIBRARIES(BundlerMatcher ${SIFTGPU_LIBRARIES} ${IL_LIBRARIES} ${GLEW_LIBRARIES} ${GLUT_LIBRARIES} ${OPENGL_LIBRARIES} )

INSTALL(TARGETS BundlerMatcher DESTINATION bin)
  