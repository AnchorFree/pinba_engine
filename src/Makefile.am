# Used to build Makefile.in

EXTRA_DIST = ha_pinba.h pinba.h pinba_types.h pinba_limits.h pinba.pb-c.h threadpool.h protobuf-c.h pinba_regenerate_report.h pinba_regenerate_report_tpl.h pinba_update_report.h pinba_update_report_tpl.h pinba_update_report_proto.h pinba_update_report_proto_tpl.h xxhash.h pinba_map.h pinba_lmap.h

AM_CPPFLAGS = $(MYSQL_INC) $(DEPS_CFLAGS) -I$(top_srcdir) -I$(top_srcdir)/sparsehash/src -I$(top_builddir)/sparsehash/src

noinst_HEADERS = ha_pinba.h pinba.h pinba_types.h pinba_limits.h pinba.pb-c.h threadpool.h protobuf-c.h pinba_regenerate_report.h pinba_update_report.h pinba_update_report_proto.h xxhash.h

lib_LTLIBRARIES = libpinba_engine.la
libpinba_engine_la_SOURCES = pinba.pb-c.c ha_pinba.cc data.cc tags.cc pool.cc main.cc threadpool.cc xxhash.c pinba_map.cc pinba_lmap.cc
libpinba_engine_la_LIBADD = $(DEPS_LIBS)
libpinba_engine_la_LDFLAGS =	-module
