if(NOT CMAKE_BUILD_TYPE)
    set(CMAKE_BUILD_TYPE "RelWithDebInfo" CACHE STRING "" FORCE)
endif()

cmake_minimum_required(VERSION 3.16)

project(thirdparty-gtsam)

set(GTSAM_ENABLE_BOOST_SERIALIZATION OFF)
set(GTSAM_USE_BOOST_FEATURES OFF)
set(GTSAM_BUILD_PYTHON OFF)
set(GTSAM_BUILD_EXAMPLES_ALWAYS OFF)
set(GTSAM_BUILD_TESTS OFF)

include(FetchContent)
fetchcontent_declare(
    gtsam
    GIT_REPOSITORY    https://github.com/borglab/gtsam
    GIT_TAG           3af5360ad397422023160604de99d0de447b0a88
)
fetchcontent_makeavailable(gtsam)
