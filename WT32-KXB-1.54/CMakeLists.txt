# The following lines of boilerplate have to be in your project's
# CMakeLists in this exact order for cmake to work correctly
cmake_minimum_required(VERSION 3.5)

#If IOT_SOLUTION_PATH is not defined, use relative path as default value
# if(NOT DEFINED ENV{IOT_SOLUTION_PATH})
#     get_filename_component(IOT_SOLUTION_PATH "~/esp/esp-iot-solution" ABSOLUTE)
#     set(ENV{IOT_SOLUTION_PATH} ${IOT_SOLUTION_PATH})
#     message(WARNING "Can't detect IOT_SOLUTION_PATH in your environment, we infer it is $ENV{IOT_SOLUTION_PATH}")
# endif()

# include($ENV{IOT_SOLUTION_PATH}/component.cmake)

include($ENV{IDF_PATH}/tools/cmake/project.cmake)

project(lvgl_example)
