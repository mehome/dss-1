server_PROGRAMS = StreamingProxy

dist_doc_DATA = StreamingProxy.html streamingproxy.conf

StreamingProxy_CPPFLAGS = ${DEBUGFLAGS} ${WARNFLAGS} ${WARNNOY2KFLAGS} -include ${top_srcdir}/PlatformHeader.h ${OPT3FLAGS} \
	-I${top_srcdir}

StreamingProxy_LDADD = \
	@SERVER_LIBS@

StreamingProxy_SOURCES = \
	get_opt.c proxy.c util.c shared_udp.c proxy_unix.c
