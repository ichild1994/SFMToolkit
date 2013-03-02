find_package(SiftGPU REQUIRED)
find_package(DevIL REQUIRED)

message("IL_INCLUDE_DIR is ${IL_INCLUDE_DIR}")
message("IL_LIBRARIES is ${IL_LIBRARIES}")

include_directories( "include/" ${SIFTGPU_INCLUDE_DIRS} ${IL_INCLUDE_DIR})

ADD_EXECUTABLE(BundlerMatcher src/main.cpp src/BundlerMatcher.cpp)

TARGET_LINK_LIBRARIES(BundlerMatcher ${SIFTGPU_LIBRARIES} ${IL_LIBRARIES})
