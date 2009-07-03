bin_PROGRAMS = PlaylistBroadcaster

PlaylistBroadcaster_CPPFLAGS = -D__USE_MAX_PRINTF__ ${DEBUGFLAGS} ${WARNFLAGS} ${WARNY2KFLAGS} -include ${top_srcdir}/PlatformHeader.h -include ${top_srcdir}/revision.h ${OPT3FLAGS} \
	-I${top_srcdir} \
	-I${top_srcdir}/QTFileLib \
	-I${top_srcdir}/OSMemoryLib \
	-I${top_srcdir}/RTSPClientLib \
	-I${top_srcdir}/APIStubLib \
	-I${top_srcdir}/APICommonCode \
	-I${top_srcdir}/CommonUtilitiesLib \
	-I${top_srcdir}/RTPMetaInfoLib

PlaylistBroadcaster_LDADD = \
	${top_builddir}/QTFileLib/libQTFileExternalLib.la \
	${top_builddir}/CommonUtilitiesLib/libCommonUtilitiesLib.la

PlaylistBroadcaster_SOURCES = \
	${top_srcdir}/CommonUtilitiesLib/daemon.c \
	${top_srcdir}/CommonUtilitiesLib/getopt.c \
	BCasterTracker.cpp \
	BroadcastLog.cpp \
	NoRepeat.cpp \
	PickerFromFile.cpp \
	PlaylistBroadcaster.cpp \
	PlaylistPicker.cpp \
	playlist_broadcaster.cpp \
	playlist_elements.cpp \
	playlist_lists.cpp \
	playlist_parsers.cpp\
	playlist_SDPGen.cpp\
	playlist_SimpleParse.cpp \
	playlist_utils.cpp\
	PLBroadcastDef.cpp \
	${top_srcdir}/APICommonCode/QTSSRollingLog.cpp \
	${top_srcdir}/RTSPClientLib/ClientSocket.cpp \
	${top_srcdir}/RTSPClientLib/RTSPClient.cpp \
	BroadcasterSession.cpp \
	${top_srcdir}/APICommonCode/SDPSourceInfo.cpp \
	${top_srcdir}/APICommonCode/SourceInfo.cpp \
	${top_srcdir}/OSMemoryLib/OSMemory.cpp \
	${top_srcdir}/RTPMetaInfoLib/RTPMetaInfoPacket.cpp
