
dssmod_LTLIBRARIES = QTSSRefMovieModule.la

QTSSRefMovieModule_la_LDFLAGS = -module -avoid-version -export-dynamic
QTSSRefMovieModule_la_CPPFLAGS = -include ${top_srcdir}/PlatformHeader.h -g -Wall -O3 \
	-I${top_srcdir}/APICommonCode \
	-I${top_srcdir}/APIModules/OSMemory_Modules \
	-I${top_srcdir}/APIStubLib \
	-I${top_srcdir}/CommonUtilitiesLib \
	-I${top_srcdir}/QTFileLib \
	-I${top_srcdir}/RTPMetaInfoLib
	
QTSSRefMovieModule_la_SOURCES = \
	${top_srcdir}/APIModules/OSMemory_Modules/OSMemory_Modules.cpp \
	${top_srcdir}/APIStubLib/QTSS_Private.cpp \
	${top_srcdir}/APICommonCode/QTSSModuleUtils.cpp\
	${top_srcdir}/APICommonCode/SDPSourceInfo.cpp \
	${top_srcdir}/APICommonCode/SourceInfo.cpp \
	${top_srcdir}/RTPMetaInfoLib/RTPMetaInfoPacket.cpp \
	QTSSRefMovieModule.cpp
	
QTSSRefMovieModule_la_LIBADD = \
	${top_builddir}/QTFileLib/libQTFileLib.la

install-data-hook:
	rm ${DESTDIR}${dssmoddir}/QTSSRefMovieModule.la
	rm ${DESTDIR}${dssmoddir}/QTSSRefMovieModule.a
