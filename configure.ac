AC_INIT(src/GLib.cs)

AC_CANONICAL_SYSTEM
AC_PREREQ(2.13)

API_VERSION=1.0
#VERSION=$API_VERSION.0
VERSION=0.3.0

AC_SUBST(API_VERSION)
AC_SUBST(VERSION)

AM_INIT_AUTOMAKE(ndesk-dbus-glib, $VERSION)

AM_MAINTAINER_MODE

AC_PROG_INSTALL

AC_PATH_PROG(PKG_CONFIG, pkg-config, no)
if test "x$PKG_CONFIG" = "xno"; then
	AC_MSG_ERROR([You need to install pkg-config])
fi
AC_SUBST(PKG_CONFIG)

MONO_REQ_VERSION=1.1.13
PKG_CHECK_MODULES(MONO, mono >= $MONO_REQ_VERSION)

AC_PATH_PROG(GMCS, gmcs, no)
if test "x$GMCS" = "xno"; then
	AC_MSG_ERROR([You need to install gmcs])
fi
AC_SUBST(GMCS)

AC_PATH_PROG(GACUTIL, gacutil, no)
if test "x$GACUTIL" = "xno"; then
	AC_MSG_ERROR([You need to install gacutil])
fi
AC_SUBST(GACUTIL)

NDESK_DBUS_REQUIRED_VERSION=0.4
PKG_CHECK_MODULES(NDESK_DBUS, ndesk-dbus-1.0 >= $NDESK_DBUS_REQUIRED_VERSION)
AC_SUBST(NDESK_DBUS_LIBS)

#GLIB_REQUIRED_VERSION=2.0
#PKG_CHECK_MODULES(GLIB, gobject-2.0 >= $GTK_REQUIRED_VERSION)
#AC_SUBST(GLIB_CFLAGS)
#AC_SUBST(GLIB_LIBS)

AC_OUTPUT([
Makefile
ndesk-dbus-glib-1.0.pc
src/AssemblyInfo.cs
src/Makefile
examples/Makefile
])
