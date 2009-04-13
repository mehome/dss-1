AC_INIT([DarwinStreamingServer],[6.0.3])
AC_CONFIG_SRCDIR([Server.tproj/main.cpp])
AC_PREFIX_DEFAULT([/opt/dss])
AM_INIT_AUTOMAKE([foreign])
AM_MAINTAINER_MODE

AC_PROG_CC
AC_PROG_CXX
AC_PROG_LIBTOOL

CPPFLAGS="-D_REENTRANT -D__USE_POSIX $CPPFLAGS"
AC_SUBST([CPPFLAGS])

AC_CHECK_HEADERS([membership.h])

AC_CHECK_FUNCS([mbr_uid_to_uuid strlcpy])

AC_CHECK_LIB([pthread],[pthread_create])
AC_CHECK_LIB([dl],[dlopen])
AC_CHECK_LIB([m],[isnan])
AC_CHECK_LIB([crypt],[crypt])

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
moviesdir=`eval echo "${datarootdir}/dss/movies"`
AC_SUBST([moviesdir])
playlistsdir=`eval echo "${datarootdir}/dss/playlists"`
AC_SUBST([playlistsdir])
serverdir=`eval echo "${sbindir}"`
AC_SUBST([serverdir])
dssdir=`eval echo "${libdir}/dss"`
AC_SUBST([dssdir])
dssmoddir=`eval echo "${libdir}/dss/modules"`
AC_SUBST([dssmoddir])
htmldir=`eval echo "${datarootdir}/dss/admin"`
AC_SUBST([htmldir])
toolsdir=`eval echo "${libexecdir}"`
AC_SUBST([toolsdir])
logdir=`eval echo "${localstatedir}/log"`
AC_SUBST([logdir])
piddir=`eval echo "${localstatedir}/run"`
AC_SUBST([piddir])
configdir=`eval echo "${sysconfdir}/dss"`
AC_SUBST([configdir])
samplesdir=`eval echo "${docdir}"`
AC_SUBST([samplesdir])

AC_CONFIG_FILES([
defaultPaths.h
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
Documentation/Makefile
])

AC_OUTPUT
