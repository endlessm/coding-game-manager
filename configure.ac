#                                               -*- Autoconf -*-
# Process this file with autoconf to produce a configure script.

AC_PREREQ([2.69])
AC_INIT([com.endlessm.Coding.Manager],
        [0.0.0],
        [bugs@endlessm.com],
        [com.endlessm.Coding.Manager],
        [http://www.endlessm.com])
AM_INIT_AUTOMAKE([1.12 dist-xz no-dist-gzip foreign tar-ustar no-define serial-tests -Wno-portability])
AM_SILENT_RULES([yes])

# Gettext package name
GETTEXT_PACKAGE=$PACKAGE
AC_SUBST(GETTEXT_PACKAGE)
AC_DEFINE_UNQUOTED(GETTEXT_PACKAGE, ["$GETTEXT_PACKAGE"],
    [Package name for Gettext])

# Gettext
AM_GNU_GETTEXT([external])
AM_GNU_GETTEXT_VERSION([0.18.1])

# Set up libtool
LT_INIT

# Set up GObject-Introspection
GOBJECT_INTROSPECTION_CHECK([1.30.0])

# Checks for programs.
GLIB_COMPILE_RESOURCES=`$PKG_CONFIG --variable glib_compile_resources gio-2.0`
AC_PATH_PROG([GJS],[gjs])

# Checks for libraries.
PKG_CHECK_MODULES(CODING_GAME_MANAGER, [glib-2.0 gio-2.0 gobject-2.0 gio-unix-2.0 gtk+-3.0])

# Checks for header files.

# Checks for typedefs, structures, and compiler characteristics.

# Checks for library functions.

# Substitute variables
AC_SUBST(GLIB_COMPILE_RESOURCES)
AC_CONFIG_FILES([
    Makefile
    po/Makefile.in
])
AC_OUTPUT
