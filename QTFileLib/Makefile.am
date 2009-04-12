
noinst_LTLIBRARIES = libQTFileLib.la libQTFileExternalLib.la

libQTFileLib_la_CPPFLAGS = -include ../PlatformHeader.h -g -Wall -O3 \
	-I${top_srcdir}/RTPMetaInfoLib \
	-I${top_srcdir}/OSMemoryLib \
	-I${top_srcdir}/APIStubLib \
	-I${top_srcdir}/CommonUtilitiesLib

libQTFileLib_la_LDFLAGS = -static

libQTFileLib_la_SOURCES = \
			QTAtom.cpp\
			QTAtom_dref.cpp \
			QTAtom_elst.cpp\
			QTAtom_hinf.cpp \
			QTAtom_mdhd.cpp\
			QTAtom_mvhd.cpp \
			QTAtom_stco.cpp\
			QTAtom_stsc.cpp \
			QTAtom_stsd.cpp\
			QTAtom_stss.cpp \
			QTAtom_stsz.cpp\
			QTAtom_stts.cpp \
			QTAtom_tkhd.cpp\
			QTAtom_tref.cpp \
			QTFile.cpp\
			QTFile_FileControlBlock.cpp \
			QTHintTrack.cpp\
			QTRTPFile.cpp \
			QTTrack.cpp
			
libQTFileExternalLib_la_CPPFLAGS = $(libQTFileLib_la_CPPFLAGS)
libQTFileExternalLib_la_LDFLAGS = -static
libQTFileExternalLib_la_SOURCES = $(libQTFileLib_SOURCES)
