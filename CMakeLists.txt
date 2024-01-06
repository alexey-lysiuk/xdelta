cmake_minimum_required(VERSION 3.0)

project(xdelta3 VERSION 3.1.0 LANGUAGES C)

# TODO: generate config.h
# TODO: lzma support
# TODO: tests

add_executable(${PROJECT_NAME}
	xdelta3/xdelta3.c
	xdelta3/xdelta3.h
	xdelta3/xdelta3-blkcache.h
	xdelta3/xdelta3-cfgs.h
	xdelta3/xdelta3-decode.h
	xdelta3/xdelta3-djw.h
	xdelta3/xdelta3-fgk.h
	xdelta3/xdelta3-hash.h
	xdelta3/xdelta3-internal.h
	xdelta3/xdelta3-list.h
	xdelta3/xdelta3-lzma.h
	xdelta3/xdelta3-main.h
	xdelta3/xdelta3-merge.h
	xdelta3/xdelta3-second.h
	xdelta3/xdelta3-test.h
)
