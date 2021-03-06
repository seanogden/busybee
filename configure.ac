#                                               -*- Autoconf -*-
# Process this file with autoconf to produce a configure script.

AC_PREREQ([2.66])
AC_INIT([BusyBee], [0.2.dev], [escriva@cs.cornell.edu])
AM_INIT_AUTOMAKE([foreign subdir-objects dist-bzip2 dist-lzma])
m4_ifdef([AM_SILENT_RULES], [AM_SILENT_RULES([yes])])
LT_PREREQ([2.2])
LT_INIT
AC_CONFIG_SRCDIR([busybee.cc])
AC_CONFIG_HEADERS([config.h])
AC_CONFIG_MACRO_DIR([m4])

# Checks for programs.
AC_PROG_CXX
AC_PROG_CC
AC_LANG(C++)

ANAL_WARNINGS_CXX

# Checks for libraries.
PKG_CHECK_MODULES([PO6], [libpo6 >= 0.2.3])
PKG_CHECK_MODULES([E], [libe >= 0.2.7])

# Checks for header files.
AC_CHECK_HEADERS([netinet/in.h stdint.h stdlib.h sys/socket.h unistd.h])

# Checks for typedefs, structures, and compiler characteristics.
AC_HEADER_STDBOOL
AC_C_INLINE
AC_TYPE_SIZE_T
AC_TYPE_SSIZE_T
AC_TYPE_UINT32_T
AC_TYPE_UINT64_T
AC_TYPE_UINT8_T
AC_EGREP_HEADER([MSG_NOSIGNAL],[sys/socket.h],AC_DEFINE([HAVE_MSG_NOSIGNAL],[1],[Defined to 1 if you have the MSG_NOSIGNAL constant]))
AC_EGREP_HEADER([SO_NOSIGPIPE],[sys/socket.h],AC_DEFINE([HAVE_SO_NOSIGPIPE],[1],[Defined to 1 if you have the SO_NOSIGPIPE constant]))

# Checks for library functions.
AC_FUNC_ERROR_AT_LINE
AC_CHECK_FUNCS([memmove socket])

AC_CONFIG_FILES([Makefile
                 busybee.pc])
AC_OUTPUT
