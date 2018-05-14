##   Makefile.am - Main Automake script.
##
##   Copyright (c) 2014, Francisco Jose Monaco  <moanco@icmc.usp.br>
##
##   This file is part of POSIXeg.
##
##   POSIXeg is free software: you can redistribute it and/or modify
##   it under the terms of the GNU General Public License as published by
##   the Free Software Foundation, either version 3 of the License, or
##   (at your option) any later version.
##
##   This program is distributed in the hope that it will be useful,
##   but WITHOUT ANY WARRANTY; without even the implied warranty of
##   MERCHANTABILITY or FITNESS FOR A PARTICULAR PURPOSE.  See the
##   GNU General Public License for more details.
##
##   You should have received a copy of the GNU General Public License
##   along with this program.  If not, see <http://www.gnu.org/licenses/>.

other_dirs = examples tools extras exercises 
install_dirs = lib

SUBDIRS = lib doc
DIST_SUBDIRS = $(SUBDIRS) $(other_dirs) 
ACLOCAL_AMFLAGS = -I m4


force-all:
	for i in $(other_dirs) ; do $(MAKE) $(AM_MAKEFLAGS) -C $$i; done

clean-local:
	for i in $(other_dirs) ; do \
	   if test -f $$i/Makefile ; then $(MAKE) $(AM_MAKEFLAGS) -C $$i clean; fi\
        done
	rm -f $(@TEMPFILES@)

install-exec-local:
	for i in $(install_dirs) ; do $(MAKE) $(AM_MAKEFLAGS) -C $$i install; done

uninstall-local:
	for i in $(install_dirs) ; do $(MAKE) $(AM_MAKEFLAGS) -C $$i uninstall; done



