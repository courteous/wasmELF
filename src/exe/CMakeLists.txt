if ("${CMAKE_BUILD_TYPE}" MATCHES "Linux")
	MESSAGE( STATUS "x86_64 LINUX COMPILER TOOLCHAIN WILL BE EXECUTED")


	add_executable(mainTestFile  main.cpp)
	
	target_link_libraries(mainTestFile my_shared_lib)
	target_compile_options(mainTestFile PUBLIC ${CMAKE_CXX_FLAGS} )
	
endif ()
