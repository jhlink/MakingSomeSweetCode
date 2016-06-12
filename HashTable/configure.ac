AC_INIT([helloworld], [0.1], [james@firstbuild.com])

AC_ARG_ENABLE(gcov,[AS_HELP_STRING([--enable-gcov], [enable coverage test])])
AC_MSG_CHECKING([whether to enable gcov])
AS_IF([test "x${enable_gcov}" = "xyes" ], AC_MSG_RESULT([yes]), AC_MSG_RESULT([no]))
AM_CONDITIONAL([ENABLEGCOV],[test "x${enable_gcov}" = "xyes"])

# Remove all optimization flags from CFLAGS
AM_CPPFLAGS="-O0"

if ENABLEGCOV
	COVERAGE_CXXFLAGS="-fprofile-arcs -ftest-coverage"
	COVERAGE_LDFLAGS="-lgcov"
endif


AM_INIT_AUTOMAKE
AC_PROG_CXXCPP
AC_CONFIG_FILES([Makefile])
AC_OUTPUT
