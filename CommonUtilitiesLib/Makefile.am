
noinst_LTLIBRARIES = libCommonUtilitiesLib.la

libCommonUtilitiesLib_la_CPPFLAGS = -include ../PlatformHeader.h ${DEBUGFLAGS} ${WARNFLAGS} ${OPTFLAGS} \
	-I${top_srcdir}/APIStubLib \
	-I${top_srcdir}/RTPMetaInfoLib \
	-I${top_srcdir}/APICommonCode

libCommonUtilitiesLib_la_SOURCES = \
	base64.c GetWord.c Trim.c md5.c \
	\
	atomic.cpp\
			ConfParser.cpp\
			DateTranslator.cpp\
			EventContext.cpp\
			IdleTask.cpp\
			MyAssert.cpp \
			OS.cpp\
			OSCodeFragment.cpp \
			OSCond.cpp\
			OSFileSource.cpp \
			OSHeap.cpp\
			OSBufferPool.cpp \
			OSMutex.cpp \
			OSMutexRW.cpp \
			OSQueue.cpp\
			OSRef.cpp \
			OSThread.cpp\
			Socket.cpp \
			SocketUtils.cpp\
			ResizeableStringFormatter.cpp \
			StringFormatter.cpp\
			StringParser.cpp \
			StringTranslator.cpp\
			StrPtrLen.cpp \
			Task.cpp\
			TCPListenerSocket.cpp\
			TCPSocket.cpp\
			TimeoutTask.cpp \
			UDPDemuxer.cpp\
			UDPSocket.cpp \
			UDPSocketPool.cpp\
			ev.cpp \
			UserAgentParser.cpp \
			QueryParamList.cpp \
			md5digest.cpp \
			SDPUtils.cpp \
			daemon.c
