cmake_minimum_required(VERSION 3.5)

project(CMakeDemo CXX)

add_executable($(PROJECT_NAME)
	main.cpp
)

find_package(OpencvCV 4 REQUIRED)

target_include_directories($(PROJECT_NAME)
	PRIVATE
	${OpenCV_INCLUDE_DIRS}
)

target_link_libraries($(PROJECT_NAME)
	PRIVATE
	${OpenCV_LIBS}
)
