cmake_minimum_required(VERSION 3.7)

project (Net_Stack LANGUAGES C)

include(FetchContent)

FetchContent_Declare(FOO 
        GIT_REPOSITORY git@github.com:yatinla/CmakeTest.git 
        GIT_TAG V8
        SOURCE_DIR ../FOO)

FetchContent_Populate(FOO)

add_executable(demo main.c ../FOO/foo.c)
