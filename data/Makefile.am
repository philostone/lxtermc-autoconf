default_config_DATA = lxtermc.conf
default_configdir = $(datadir)/lxtermc

uidir=$(datadir)/lxtermc
ui_in_files= \
	lxtermc-preferences.glade

ui_files = $(ui_in_files:.glade=.ui)

ui_DATA = $(ui_files) menu.ui

# Purge GtkBuilder UI files
.glade.ui:
	sed 's/<!--.*-->//' < $< | sed ':a;N;$$!ba;s/ *\n *</</g' > $@

CLEANFILES = $(ui_files)

lxtermc.desktop_in_files = lxtermc.desktop.in
lxtermc.desktop.in_DATA = $(lxtermc.desktop_in_files:.desktop.in=.desktop)
#@INTLTOOL_DESKTOP_RULE@
lxtermc.desktop.indir = $(datadir)/applications

lxtermc_images_DATA = lxtermc.png
lxtermc_imagesdir = $(datadir)/icons/hicolor/128x128/apps

EXTRA_DIST = \
	lxtermc.conf.in \
	$(lxtermc_images_DATA) \
	$(lxtermc.desktop_in_files) \
	$(lxtermc.desktop.in_DATA) \
	$(ui_DATA) \
	$(ui_in_files) \
	$(default_config_DATA)
