######################################################################
# Makefile.am                                                 May 2000
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

SUBDIRS = libvanessa_adt test debian

EXTRA_DIST = autogen.sh libvanessa_adt1.spec

clean-local:
	rm -f build-stamp

pkgconfigdir = $(libdir)/pkgconfig
pkgconfig_DATA = vanessa-adt.pc
