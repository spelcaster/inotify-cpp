project (InotifyUnitTest)

###############################################################################
# Boost
###############################################################################
find_package(Boost 1.61.0 COMPONENTS system filesystem unit_test_framework REQUIRED)
include_directories(SYSTEM ${Boost_INCLUDE_DIRS})

###############################################################################
# Thread
###############################################################################
find_package (Threads)


add_executable (inotify_unit_test main.cpp NotifierBuilderTests.cpp)
target_link_libraries (inotify_unit_test LINK_PUBLIC
        Inotify
        ${Boost_LIBRARIES}
        ${CMAKE_THREAD_LIBS_INIT})