lib_LTLIBRARIES = libxshmfence.la

FUTEX_SOURCES=xshmfence_futex.c xshmfence_futex.h

libxshmfence_la_SOURCES = \
	xshmfenceint.h \
	xshmfence_alloc.c \
	$(FUTEX_SOURCES)

AM_CFLAGS = $(CWARNFLAGS)

libxshmfence_la_LDFLAGS = -version-number 1:0:0 -no-undefined

libxshmfenceincludedir = $(includedir)/X11
libxshmfenceinclude_HEADERS = xshmfence.h

if LINT
ALL_LINT_FLAGS=$(LINT_FLAGS) $(DEFS) $(DEFAULT_INCLUDES) $(INCLUDES) \
		$(AM_CPPFLAGS) $(CPPFLAGS)

lint:
	$(LINT) $(ALL_LINT_FLAGS) $(libxshmfence_la_SOURCES) $(LIBS)
endif LINT
