## Process this file with automake to produce Makefile.in

bin_PROGRAMS = lxtermc

lxtermc_CPPFLAGS = \
	-I$(top_srcdir) \
	-DPACKAGE_BIN_DIR=\""$(bindir)"\" \
	-DPACKAGE_DATA_DIR=\""$(datadir)"\" \
	-DPACKAGE_LOCALE_DIR=\""$(localedir)"\" \
	$(PACKAGE_CFLAGS) \
	$(ADDITIONAL_FLAGS) \
	$(G_CAST_CHECKS)

lxtermc_SOURCES = \
	unixsocket.h \
	unixsocket.c \
	setting.h \
	setting.c \
	lxtermc.h \
	lxtermc.c \
	preferences.h \
	preferences.c

lxtermc_LDADD = \
		$(PACKAGE_LIBS) \
		$(INTLLIBS)
