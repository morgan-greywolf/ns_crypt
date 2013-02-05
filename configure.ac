AC_INIT(ns_crypt, version-0.1)
echo -e "Testing for a C compiler ... "
AC_PROG_CC
AC_LANG(C)
AC_CHECK_LIB(crypt)
AC_CHECK_HEADER(crypt.h, [AC_DEFINE([NEED_CRYPT_H])])
AC_CHECK_HEADER(unistd.h)
AC_CHECK_HEADER(ctype.h)
AC_CHECK_HEADER(syslog.h)
AC_CHECK_HEADER(sys/timne.h)
AC_CHECK_HEADER(stdlib.h)
AC_CHECK_HEADER(errno.h)
AC_CHECK_TYPE(boolean_t, [], [echo 'typedef enum { B_FALSE, B_TRUE } boolean_t;' >>confdefs.h])
AC_SEARCH_LIBS([crypt], [crypt],
                [AC_DEFINE([HAVE_CRYPT], [], 
                          [Define this if your system has a crypt() function])])
AC_SUBST([CRYPT_LIB])
cp confdefs.h config.h
AC_OUTPUT(Makefile)
