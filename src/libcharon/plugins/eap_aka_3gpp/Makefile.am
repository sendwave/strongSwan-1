AM_CPPFLAGS = \
	-I$(top_srcdir)/src/libstrongswan \
	-I$(top_srcdir)/src/libcharon \
	-I$(top_srcdir)/src/libsimaka

AM_CFLAGS = \
	$(PLUGIN_CFLAGS)

libstrongswan_eap_aka_3gpp_la_LDFLAGS = -module -avoid-version

if MONOLITHIC
noinst_LTLIBRARIES = libstrongswan-eap-aka-3gpp.la
else
plugin_LTLIBRARIES = libstrongswan-eap-aka-3gpp.la
libstrongswan_eap_aka_3gpp_la_LIBADD = $(top_builddir)/src/libsimaka/libsimaka.la
endif

libstrongswan_eap_aka_3gpp_la_SOURCES = \
	eap_aka_3gpp_plugin.h eap_aka_3gpp_plugin.c \
	eap_aka_3gpp_card.h eap_aka_3gpp_card.c \
	eap_aka_3gpp_provider.h eap_aka_3gpp_provider.c \
	eap_aka_3gpp_functions.h eap_aka_3gpp_functions.c
