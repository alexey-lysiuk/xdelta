cmake_minimum_required(VERSION 3.0)

project(xdelta3 VERSION 3.1.0 LANGUAGES C)

# TODO: generate config.h
# TODO: lzma support
# TODO: tests

include(CheckTypeSize)

check_type_size("size_t" SIZEOF_SIZE_T)
check_type_size("unsigned long long" SIZEOF_UNSIGNED_LONG_LONG)

add_executable(${PROJECT_NAME}
	xdelta3.c
	xdelta3.h
	xdelta3-blkcache.h
	xdelta3-cfgs.h
	xdelta3-decode.h
	xdelta3-djw.h
	xdelta3-fgk.h
	xdelta3-hash.h
	xdelta3-internal.h
	xdelta3-list.h
	xdelta3-lzma.h
	xdelta3-main.h
	xdelta3-merge.h
	xdelta3-second.h
	xdelta3-test.h
)

#set_property(TARGET ${PROJECT_NAME} PROPERTY C_STANDARD 23)

target_compile_definitions(${PROJECT_NAME} PRIVATE
	SIZEOF_SIZE_T=${SIZEOF_SIZE_T}
	SIZEOF_UNSIGNED_LONG_LONG=${SIZEOF_UNSIGNED_LONG_LONG}
	XD3_MAIN
)
