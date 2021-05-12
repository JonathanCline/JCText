project("jctext" VERSION 0.0.1)

set(lib_cxx 20)

set(lib_public_include
	"include")

set(lib_private_include
	"source")
	
set(lib_public_link
	jclib)

set(lib_private_link
	freetype)

add_library(${PROJECT_NAME} STATIC "include/${PROJECT_NAME}.h" "source/${PROJECT_NAME}.cpp")
target_include_directories(${PROJECT_NAME} PUBLIC ${lib_public_include} PRIVATE ${lib_private_include})
target_link_libraries(${PROJECT_NAME} PUBLIC ${lib_public_link} PRIVATE ${lib_private_link})
set_target_properties(${PROJECT_NAME} PROPERTIES CXX_STANDARD ${lib_cxx} CXX_STANDARD_REQUIRED True)
