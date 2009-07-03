AC_INIT([DarwinStreamingServer],[6.0.3-evo1],,[dss])
AC_CONFIG_SRCDIR([Server.tproj/main.cpp])
AM_INIT_AUTOMAKE([foreign])
AM_MAINTAINER_MODE
JL_CHECK_BUNDLES
AC_PROG_CC
AC_PROG_CXX
AC_PROG_LIBTOOL

case "${host_os}" in
	darwin*)
		fs_layout="apple"
		fs_domain=""
		CPPFLAGS="-D__MacOSX__ -DNeXT $CPPFLAGS"
		CXXFLAGS="-fmessage-length=0 -Wno-trigraphs -fno-exceptions -fpascal-strings -fasm-blocks"
		SERVER_LIBS="-framework Security -framework CoreFoundation -framework DirectoryService"
		test x"${localstatedir}" = x'${prefix}/var' && localstatedir='/var'
		;;
	*)
		fs_layout="gnu"
		;;
esac

case "${host_os}" in
	linux-gnu*)
		HOST_OS=linux
		;;
	solaris*)
		HOST_OS=solaris
		;;
	darwin*)
		HOST_OS=darwin
		;;
	freebsd*)
		HOST_OS=freebsd
		;;
	netbsd*)
		HOST_OS=netbsd
		;;
	openbsd*)
		HOST_OS=openbsd
		;;
	*)
		HOST_OS=`echo $host_os | sed -e 's%-%_%g'`
		;;
esac

host_os_def="host_os_${HOST_OS}"
host_cpu_def="host_cpu_${host_cpu}"

CPPFLAGS="-D_REENTRANT -D__USE_POSIX $CPPFLAGS -D${host_os_def} -D${host_cpu_def}"
AC_SUBST([CPPFLAGS])

AC_SUBST([CXXFLAGS])

AC_SUBST([SERVER_LIBS])

AC_C_BIGENDIAN

AC_HEADER_TIME
AC_CHECK_HEADERS([membership.h errno.h sys/errno.h sys/types.h netinet/in.h pthread.h sys/sockio.h ifaddrs.h paths.h sys/sysctl.h])
AC_CHECK_HEADERS([crypt.h])

AC_CHECK_LIB([pthread],[pthread_create])
AC_CHECK_LIB([dl],[dlopen])
AC_CHECK_LIB([m],[isnan])
AC_CHECK_LIB([crypt],[crypt])
AC_CHECK_LIB([nsl],[gethostbyname])
AC_CHECK_LIB([socket],[socket])

AC_CHECK_FUNCS([mbr_uid_to_uuid strlcpy pthread_create daemon])

AC_CHECK_MEMBER([struct tm.tm_gmtoff],[AC_DEFINE([HAVE_TM_GMTOFF],1)])

dnl User and group to run the server as
dssuser="qtss"
dssgroup="qtss"
AC_SUBST([dssuser])
AC_SUBST([dssgroup])

if test x"$prefix" = x"NONE" ; then
	prefix="${ac_default_prefix}"
fi
if test x"$exec_prefix" = x"NONE" ; then
	exec_prefix="${prefix}"
fi

dnl Evaluate the full paths to various directories so that we can substitute
dnl them into configuration files and scripts.

if test x"${jl_enable_bundles}" = x"yes" ; then
	fs_layout="apple"
fi

if test x"${fs_layout}" = x"gnu" ; then
	moviesdir=`eval echo "${datarootdir}/${PACKAGE_TARNAME}/movies"`
	playlistsdir=`eval echo "${datarootdir}/${PACKAGE_TARNAME}/playlists"`
	serverdir=`eval echo "${sbindir}"`
	dssdir=`eval echo "${libdir}/${PACKAGE_TARNAME}"`
	dssmoddir=`eval echo "${libdir}/${PACKAGE_TARNAME}/modules"`
	htmldir=`eval echo "${datarootdir}/${PACKAGE_TARNAME}/admin"`
	toolsdir=`eval echo "${libexecdir}"`
	logdir=`eval echo "${localstatedir}/log/${PACKAGE_TARNAME}"`
	piddir=`eval echo "${localstatedir}/run"`
	configdir=`eval echo "${sysconfdir}/${PACKAGE_TARNAME}"`
	samplesdir=`eval echo "${docdir}"`
else
	base=`eval echo "${librarydir}/${PACKAGE_NAME}"`
	moviesdir=`eval echo "${base}/Movies"`
	playlistsdir=`eval echo "${base}/Playlists"`
	serverdir=`eval echo "${sbindir}"`
	dssdir=`eval echo "${base}"`
	dssmoddir=`eval echo "${base}/Modules"`
	toolsdir=`eval echo "${sbindir}"`
	logdir=`eval echo "${base}/Logs"`
	piddir=`eval echo "${localstatedir}/run"`
	configdir=`eval echo "${base}/Config"`
	samplesdir="{$moviesdir}"
fi

AC_SUBST([moviesdir])
AC_SUBST([playlistsdir])
AC_SUBST([serverdir])
AC_SUBST([dssdir])
AC_SUBST([dssmoddir])
AC_SUBST([htmldir])
AC_SUBST([toolsdir])
AC_SUBST([logdir])
AC_SUBST([piddir])
AC_SUBST([configdir])
AC_SUBST([samplesdir])

AC_DEFINE_UNQUOTED([kPlatformNameString], ["$host_os"], [Platform name])

AC_CONFIG_FILES([
defaultPaths.h
revision.h
Makefile
CommonUtilitiesLib/Makefile
QTFileLib/Makefile
Server.tproj/Makefile
APIModules/Makefile
APIModules/QTSSRefMovieModule/Makefile
streamingserver.xml
WebAdmin/streamingadminserver.conf
initscripts/dss
initscripts/Makefile
PlaylistBroadcaster.tproj/Makefile
StreamingProxy.tproj/Makefile
Documentation/Makefile
])

AC_OUTPUT

AC_MSG_RESULT([

Installation paths summary:

Server:                 $serverdir
QTSS Modules:           $dssmoddir
Tools:                  $toolsdir
Configuration files:    $configdir
Movies:                 $moviesdir
Playlists:              $playlistsdir
])
