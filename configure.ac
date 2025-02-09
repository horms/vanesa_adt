dnl vanessa_adt
dnl Library of Abstract Data Types
dnl Copyright (C) 1999-2008  Simon Horman <horms@verge.net.au>
dnl 
dnl This library is free software; you can redistribute it and/or modify it
dnl under the terms of the GNU Lesser General Public License as published by
dnl the Free Software Foundation; either version 2 of the License, or (at
dnl your option) any later version.
dnl 
dnl This library is distributed in the hope that it will be useful, but
dnl WITHOUT ANY WARRANTY; without even the implied warranty of
dnl MERCHANTABILITY or FITNESS FOR A PARTICULAR PURPOSE.  See the GNU Lesser
dnl General Public License for more details.
dnl 
dnl You should have received a copy of the GNU Lesser General Public License
dnl along with this library; if not, write to the Free Software Foundation,
dnl Inc., 59 Temple Place, Suite 330, Boston, MA  02111-1307 USA


AC_INIT(libvanessa_adt/vanessa_adt.h)
AM_CONFIG_HEADER(config.h)

AC_CONFIG_MACRO_DIR([libltdl/m4])
m4_ifdef([AM_SILENT_RULES], [AM_SILENT_RULES([yes])])
LT_INIT
LTDL_INIT
AM_INIT_AUTOMAKE(vanessa_adt, 0.0.9)

AC_PROG_LIBTOOL
AC_PROG_CC
AC_PROG_INSTALL
AC_PROG_LN_S
AC_PROG_MAKE_SET

dnl Checks for libraries.
dnl Checks for header files.
AC_HEADER_STDC
AC_HEADER_SYS_WAIT

dnl Checks for typedefs, structures, and compiler characteristics.
AC_TYPE_UID_T
AC_TYPE_SIZE_T

dnl Checks for library functions.
AC_TYPE_SIGNAL
AC_FUNC_WAIT3
AC_CHECK_FUNCS(flim)

AC_MSG_CHECKING("for Linux style shared object linking")
if test "$host_os" = "linux" -o "$host_os" = "linux-gnu"; then
  AC_MSG_RESULT(Yes)
  extra_libs=""
else
  AC_MSG_RESULT(No)
  extra_libs="-lvanessa_logger"
fi
AC_SUBST(extra_libs)

AC_CHECK_LIB(
  vanessa_logger,
  vanessa_logger_closelog,
  :,
  AC_MSG_ERROR(
    ""
    "**********************************************************************"
    "* vanessa_adt requires the vanessa_logger generic logging library"
    "* available from"
    "* http://www.vergenet.net/linux/vanessa/ and mirrors."
    "**********************************************************************"
  ) ;\
)

AC_OUTPUT(
debian/Makefile 
libvanessa_adt/Makefile 
test/Makefile 
Makefile
libvanessa_adt1.spec
INSTALL
vanessa-adt.pc
)
