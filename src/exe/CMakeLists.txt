if ("${CMAKE_BUILD_TYPE}" MATCHES "Linux")
	MESSAGE( STATUS "x86_64 LINUX COMPILER TOOLCHAIN WILL BE EXECUTED")
	set(CMAKE_SYSTEM_NAME Linux)
#	set(CMAKE_SYSTEM_PROCESSOR x86_64)
	SET(TARGET x86_64-unknown-linux-gnu)

	set(CMAKE_C_COMPILER clang)
	set(CMAKE_CXX_COMPILER clang++)

	#set(triple x86_64-unknown-linux-gnu)
	#set(CMAKE_CXX_COMPILER_TARGET ${triple})
	#set(CMAKE_C_COMPILER_TARGET ${triple})


	add_executable(mainTestFile  main.cpp)
	
	target_link_libraries(mainTestFile my_shared_lib)
	target_compile_options(mainTestFile PUBLIC ${CMAKE_CXX_FLAGS} )
	
endif ()

