ACLOCAL_AMFLAGS=-I m4

#######################################
# The list of libraries we are building seperated by spaces.
# The 'lib_' indicates that these build products will be installed
# in the $(libdir) directory. For example /usr/lib
lib_LTLIBRARIES = libbswabe.la

#######################################
# Build information for each library

# Sources for libbswabe
libbswabe_la_SOURCES = core.c misc.c

include_HEADERS = bswabe.h

# Linker options libTestProgram
libbswabe_la_LDFLAGS = -no-undefined \
-L$(top_srcdir)/../openssl_install/lib \
-L$(top_srcdir)/../gmp_install/lib \
-L$(top_srcdir)/../glib_install/lib \
-L$(top_srcdir)/../pbc_install/lib

libbswabe_la_LIBADD = -lglib-2.0 -lgmp -lpbc -lcrypto

# Compiler options. Here we are adding the include directory
# to be searched for headers included in the source code.
libbswabe_la_CPPFLAGS = \
-I$(top_srcdir)/../openssl_install/include \
-I$(top_srcdir)/../gmp_install/include \
-I$(top_srcdir)/../glib_install/lib/glib-2.0/include \
-I$(top_srcdir)/../glib_install/include/glib-2.0 \
-I$(top_srcdir)/../pbc_install/include/pbc

