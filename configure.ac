#                                               -*- Autoconf -*-
# Process this file with autoconf to produce a configure script.
AC_PREREQ([2.57])


AC_INIT([xvfb-run],[0.05],[opticsoft@head.cfa.harvard.edu],[xvfb-run])
AM_INIT_AUTOMAKE( [check-news] )
AC_CONFIG_SRCDIR([src/xvfb-run.in])

AC_PROG_INSTALL

AC_CHECK_PROG([HAVE_xauth],[xauth],[yes],[no] )
test $HAVE_xauth = no && AC_MSG_ERROR([missing xauth])

AC_CHECK_PROG([HAVE_timeout],[timeout],[yes],[no] )
test $HAVE_timeout = no && AC_MSG_ERROR([missing timeout])

AC_CHECK_PROG([HAVE_Xvfb],[Xvfb],[yes], [no] )
test $HAVE_Xvfb = no && AC_MSG_ERROR([missing Xvfb])

AC_CHECK_PROG([HAVE_setsid],[setsid],[yes], [no] )
test $HAVE_setsid = no && AC_MSG_ERROR([missing setsid])

AC_CHECK_PROG([HAVE_mktemp],[mktemp],[yes], [no] )
test $HAVE_mktemp = no && AC_MSG_ERROR([missing mktemp])

AC_CONFIG_FILES([ Makefile ])
AC_CONFIG_FILES([src/xvfb-run],[chmod +x src/xvfb-run])
AC_CONFIG_FILES([man/xvfb-run.1])
AC_OUTPUT
