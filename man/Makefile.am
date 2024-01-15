man_MANS = \
	lxtermc.1

man_XMANS = \
	lxtermc.xml

EXTRA_DIST = \
	$(man_MANS) \
	$(man_XMANS)


if ENABLE_REGENERATE_MAN

lxtermc.1: lxtermc.xml
	$(XSLTPROC) -nonet http://docbook.sourceforge.net/release/xsl/current/manpages/docbook.xsl $<

CLEANFILES = $(man_MANS) 
else

$(man_MANS):
	@echo ""
	@echo "Error: you need to run configure with '--enable-man'"
	@echo "       in order to regenerate man pages."
	@echo ""
	@false
endif


