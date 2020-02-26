AC_INIT([stomp], [0.1], [evgeni@studio-punkt.com],[],[https://github.com/evgenido/stomp])
AC_CONFIG_MACRO_DIR([m4])
AM_INIT_AUTOMAKE([-Wall foreign])
AM_SILENT_RULES([yes])
LT_INIT
AC_PROG_CC

m4_define_default([PKG_PROG_PKG_CONFIG],
  [AC_MSG_CHECKING([pkg-config])
  AC_MSG_RESULT([no])])

PKG_PROG_PKG_CONFIG

m4_define_default([PKG_CHECK_MODULES],
  [AC_MSG_CHECKING([$1])
   AC_MSG_RESULT([no])
   $4])

PKG_CHECK_MODULES(CHECK,[check], [HAVE_CHECK=yes], [HAVE_CHECK=no])
AM_CONDITIONAL(HAVE_CHECK, test x$HAVE_CHECK = xyes)

AC_SUBST([STOMP_SO_VERSION], [0:0:0])

AC_CONFIG_FILES([Makefile src/Makefile tests/Makefile examples/Makefile stomp.pc])
AC_OUTPUT
