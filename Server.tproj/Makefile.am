server_PROGRAMS = DarwinStreamingServer

DarwinStreamingServer_LDFLAGS = -export-dynamic

DarwinStreamingServer_CPPFLAGS = -DDSS_USE_API_CALLBACKS -g -Wall -Wno-format-y2k -include ../PlatformHeader.h -O3 \
	-I${top_srcdir} \
	-I${top_srcdir}/QTFileLib \
	-I${top_srcdir}/OSMemoryLib \
	-I${top_srcdir}/RTSPClientLib \
	-I${top_srcdir}/APIModules \
	-I${top_srcdir}/APICommonCode \
	-I${top_srcdir}/APIModules/OSMemory_Modules \
	-I${top_srcdir}/APIModules/QTSSAccessLogModule \
	-I${top_srcdir}/APIModules/QTSSFileModule \
	-I${top_srcdir}/APIModules/QTSSFlowControlModule \
	-I${top_srcdir}/APIModules/QTSSReflectorModule \
	-I${top_srcdir}/APIModules/QTSSSvrControlModule \
	-I${top_srcdir}/APIModules/QTSSWebDebugModule \
	-I${top_srcdir}/APIModules/QTSSWebStatsModule \
	-I${top_srcdir}/APIModules/QTSSAuthorizeModule \
	-I${top_srcdir}/APIModules/QTSSPOSIXFileSysModule \
	-I${top_srcdir}/APIModules/QTSSAdminModule \
	-I${top_srcdir}/APIModules/QTSSMP3StreamingModule \
	-I${top_srcdir}/APIModules/QTSSRTPFileModule \
	-I${top_srcdir}/APIModules/QTSSAccessModule \
	-I${top_srcdir}/APIModules/QTSSHttpFileModule \
	-I${top_srcdir}/QTFileTools/RTPFileGen.tproj \
	-I${top_srcdir}/APIStubLib \
	-I${top_srcdir}/CommonUtilitiesLib \
	-I${top_srcdir}/RTCPUtilitiesLib \
	-I${top_srcdir}/HTTPUtilitiesLib \
	-I${top_srcdir}/RTPMetaInfoLib \
	-I${top_srcdir}/PrefsSourceLib \
	-I${top_srcdir}/Server.tproj

DarwinStreamingServer_LDADD = \
	${top_builddir}/CommonUtilitiesLib/libCommonUtilitiesLib.la \
	${top_builddir}/QTFileLib/libQTFileLib.la

DarwinStreamingServer_SOURCES = \
	${top_srcdir}/CommonUtilitiesLib/daemon.c \
	QTSSExpirationDate.cpp\
			QTSSCallbacks.cpp \
			QTSSDictionary.cpp\
			QTSSDataConverter.cpp \
			QTSSErrorLogModule.cpp \
			QTSSMessages.cpp\
			QTSSModule.cpp \
			QTSServerPrefs.cpp\
			QTSSSocket.cpp\
			QTSSFile.cpp\
			QTSSPrefs.cpp \
			QTSServer.cpp\
			QTSServerInterface.cpp \
			RTCPTask.cpp\
			RTPSession.cpp \
			RTPPacketResender.cpp \
			RTPBandwidthTracker.cpp \
			RTPOverbufferWindow.cpp \
			RTPSessionInterface.cpp\
			RTPStream.cpp \
			RTSPProtocol.cpp\
			RTSPRequest.cpp \
			RTSPRequestInterface.cpp\
			RTSPRequestStream.cpp \
			RTSPResponseStream.cpp\
			RTSPSession.cpp \
			RTSPSessionInterface.cpp\
			RTPSession3GPP.cpp\
			RTPStream3gpp.cpp\
			RTSPRequest3GPP.cpp\
			RTSPSession3GPP.cpp\
			main.cpp \
			RunServer.cpp \
			GenerateXMLPrefs.cpp \
			QTSSUserProfile.cpp\
			\
			${top_srcdir}/PrefsSourceLib/FilePrefsSource.cpp\
			${top_srcdir}/PrefsSourceLib/XMLPrefsParser.cpp \
			${top_srcdir}/PrefsSourceLib/XMLParser.cpp \
			${top_srcdir}/OSMemoryLib/OSMemory.cpp \
			${top_srcdir}/RTSPClientLib/RTSPClient.cpp \
			${top_srcdir}/RTSPClientLib/ClientSocket.cpp \
			${top_srcdir}/HTTPUtilitiesLib/HTTPProtocol.cpp \
			${top_srcdir}/HTTPUtilitiesLib/HTTPRequest.cpp \
			${top_srcdir}/RTCPUtilitiesLib/RTCPAPPPacket.cpp\
			${top_srcdir}/RTCPUtilitiesLib/RTCPPacket.cpp \
			${top_srcdir}/RTCPUtilitiesLib/RTCPSRPacket.cpp\
			${top_srcdir}/RTCPUtilitiesLib/RTCPAckPacket.cpp\
			${top_srcdir}/RTCPUtilitiesLib/RTCPAPPNADUPacket.cpp\
			${top_srcdir}/RTCPUtilitiesLib/RTCPAPPQTSSPacket.cpp\
			${top_srcdir}/RTPMetaInfoLib/RTPMetaInfoPacket.cpp\
			${top_srcdir}/APIStubLib/QTSS_Private.cpp \
			${top_srcdir}/APICommonCode/QTSSModuleUtils.cpp\
			${top_srcdir}/APICommonCode/QTSSRollingLog.cpp \
			${top_srcdir}/APICommonCode/SDPSourceInfo.cpp \
			${top_srcdir}/APICommonCode/SourceInfo.cpp \
			${top_srcdir}/APICommonCode/QTAccessFile.cpp \
			${top_srcdir}/APICommonCode/QTSS3GPPModuleUtils.cpp\
			${top_srcdir}/SafeStdLib/InternalStdLib.cpp \
			${top_srcdir}/APIModules/QTSSAccessLogModule/QTSSAccessLogModule.cpp \
			${top_srcdir}/APIModules/QTSSFileModule/QTSSFileModule.cpp \
			${top_srcdir}/APIModules/QTSSFlowControlModule/QTSSFlowControlModule.cpp \
			${top_srcdir}/APIModules/QTSSReflectorModule/QTSSReflectorModule.cpp \
			${top_srcdir}/APIModules/QTSSReflectorModule/QTSSRelayModule.cpp \
			${top_srcdir}/APIModules/QTSSReflectorModule/ReflectorSession.cpp\
			${top_srcdir}/APIModules/QTSSReflectorModule/RelaySession.cpp\
			${top_srcdir}/APIModules/QTSSReflectorModule/ReflectorStream.cpp\
			${top_srcdir}/APIModules/QTSSReflectorModule/RCFSourceInfo.cpp \
			${top_srcdir}/APIModules/QTSSReflectorModule/RTSPSourceInfo.cpp \
			${top_srcdir}/APIModules/QTSSReflectorModule/RelayOutput.cpp \
			${top_srcdir}/APIModules/QTSSReflectorModule/RelaySDPSourceInfo.cpp \
			${top_srcdir}/APIModules/QTSSReflectorModule/RTPSessionOutput.cpp \
			${top_srcdir}/APIModules/QTSSReflectorModule/SequenceNumberMap.cpp \
			${top_srcdir}/APIModules/QTSSWebDebugModule/QTSSWebDebugModule.cpp \
			${top_srcdir}/APIModules/QTSSWebStatsModule/QTSSWebStatsModule.cpp \
			${top_srcdir}/APIModules/QTSSPOSIXFileSysModule/QTSSPosixFileSysModule.cpp \
			${top_srcdir}/APIModules/QTSSAdminModule/AdminElementNode.cpp \
			${top_srcdir}/APIModules/QTSSAdminModule/AdminQuery.cpp \
			${top_srcdir}/APIModules/QTSSAdminModule/QTSSAdminModule.cpp \
			${top_srcdir}/APIModules/QTSSMP3StreamingModule/QTSSMP3StreamingModule.cpp \
			${top_srcdir}/APIModules/QTSSRTPFileModule/QTSSRTPFileModule.cpp \
			${top_srcdir}/APIModules/QTSSRTPFileModule/RTPFileSession.cpp \
			${top_srcdir}/APIModules/QTSSAccessModule/QTSSAccessModule.cpp \
			${top_srcdir}/APIModules/QTSSHttpFileModule/QTSSHttpFileModule.cpp \
			${top_srcdir}/APIModules/QTSSAccessModule/AccessChecker.cpp
