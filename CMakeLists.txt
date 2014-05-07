cmake_minimum_required(VERSION 2.8.3)
project(asl_cmake)

find_package(catkin_simple REQUIRED)

catkin_simple()


FILE(GLOB files "${CMAKE_CURRENT_SOURCE_DIR}/cmake/*.cmake")

cs_install()
install(FILES ${files}
        DESTINATION ${CATKIN_PACKAGE_SHARE_DESTINATION}/cmake
)

cs_export(CFG_EXTRAS ${files})


message("Files: ${files}")
message("Install: ${CATKIN_PACKAGE_SHARE_DESTINATION}")
