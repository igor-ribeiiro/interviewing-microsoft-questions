cmake_minimum_required(VERSION 3.9)
project(interview_questions)

set(CMAKE_CXX_STANDARD 14)

file(GLOB_RECURSE SRCS *.cpp)
foreach (file_path ${SRCS})
    get_filename_component(dir_path ${file_path} PATH)
    get_filename_component(file_name_we ${file_path} NAME_WE)

    add_executable(${file_name_we} ${file_path})
endforeach ()