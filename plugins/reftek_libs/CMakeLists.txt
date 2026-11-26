ADD_COMPILE_DEFINITIONS(LINUX _REENTRANT unix)

# archive subdirectory
# CC: This is broken on modern Linux and not used by the plugin, so skip it completely.
#ADD_LIBRARY(reftek_archive STATIC
#	archive/archive.c
#	archive/create.c
#	archive/errors.c
#	archive/evnfiles.c
#	archive/find.c
#	archive/linklist.c
#	archive/open.c
#	archive/purge.c
#	archive/rate.c
#	archive/read.c
#	archive/recfmt.c
#	archive/serialize.c
#	archive/state.c
#	archive/streams.c
#	archive/strlist.c
#	archive/unix.c
#	archive/write.c)
#TARGET_INCLUDE_DIRECTORIES(reftek_archive PUBLIC $<BUILD_INTERFACE:${CMAKE_CURRENT_SOURCE_DIR}/include>)

# msgq subdirectory
ADD_LIBRARY(reftek_msgq STATIC
	msgq/msgq.c)
TARGET_INCLUDE_DIRECTORIES(reftek_msgq PUBLIC $<BUILD_INTERFACE:${CMAKE_CURRENT_SOURCE_DIR}/include>)

# reftek subdirectory
ADD_LIBRARY(reftek_libreftek STATIC
	reftek/ad.c
	reftek/cd.c
	reftek/ds.c
	reftek/dt.c
	reftek/eh.c
	reftek/et.c
	reftek/om.c
	reftek/sh.c
	reftek/sc.c
	reftek/com.c
	reftek/type.c
	reftek/steim.c
	reftek/string.c)
TARGET_INCLUDE_DIRECTORIES(reftek_libreftek PUBLIC $<BUILD_INTERFACE:${CMAKE_CURRENT_SOURCE_DIR}/include>)

# rtp subdirectory
ADD_LIBRARY(reftek_rtp STATIC
	rtp/accept.c
	rtp/attr.c
	rtp/close.c
	rtp/cmdpkt.c
	rtp/log.c
	rtp/misc.c
	rtp/open.c
	rtp/pid.c
	rtp/recv.c
	rtp/send.c
	rtp/server.c
	rtp/soh.c
	rtp/stat.c
	rtp/version.c)
TARGET_INCLUDE_DIRECTORIES(reftek_rtp PUBLIC $<BUILD_INTERFACE:${CMAKE_CURRENT_SOURCE_DIR}/include>)

# si subdirectory
# CC: This is broken on modern Linux and not used by the plugin, so skip it completely.
#ADD_LIBRARY(reftek_si STATIC
#	si/si.c)
#TARGET_INCLUDE_DIRECTORIES(reftek_si PUBLIC $<BUILD_INTERFACE:${CMAKE_CURRENT_SOURCE_DIR}/include>)

# util subdirectory
ADD_LIBRARY(reftek_util STATIC
	util/bcd2long.c
	util/dump.c
	util/getline.c
	util/find.c
	util/mstime.c
	util/parse.c
	util/string.c
	util/swap.c
	util/timer.c
	util/timefunc.c)
TARGET_INCLUDE_DIRECTORIES(reftek_util PUBLIC $<BUILD_INTERFACE:${CMAKE_CURRENT_SOURCE_DIR}/include>)
