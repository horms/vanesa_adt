######################################################################
# Makefile.am                                           September 2000
# Simon Horman                                      horms@verge.net.au
#
# vanessa_adt
# Library of Abstract Data Types
# Copyright (C) 1999-2008  Simon Horman <horms@verge.net.au>
# 
# This library is free software; you can redistribute it and/or
# modify it under the terms of the GNU Lesser General Public License
# as published by the Free Software Foundation; either version 2 of
# the License, or (at your option) any later version.
# 
# This library is distributed in the hope that it will be useful, but
# WITHOUT ANY WARRANTY; without even the implied warranty of
# MERCHANTABILITY or FITNESS FOR A PARTICULAR PURPOSE.  See the GNU
# Lesser General Public License for more details.
# 
# You should have received a copy of the GNU Lesser General Public
# License along with this library; if not, write to the Free Software
# Foundation, Inc., 59 Temple Place, Suite 330, Boston, MA
# 02111-1307 USA
#
######################################################################

noinst_PROGRAMS = dynamic_array_test list_test hash_test config_file_test

dynamic_array_test_SOURCES = dynamic_array_test.c

list_test_SOURCES = list_test.c

hash_test_SOURCES = hash_test.c

config_file_test_SOURCES = config_file_test.c

INCLUDES= -I$(top_srcdir)/libvanessa_adt

LDADD = \
-lvanessa_logger \
-L../libvanessa_adt \
-L../libvanessa_adt/.libs/ \
-lvanessa_adt \
@extra_libs@
