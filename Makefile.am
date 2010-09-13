#  Copyright 2005 Red Hat, Inc.
# 
#  Permission to use, copy, modify, distribute, and sell this software
#  and its documentation for any purpose is hereby granted without fee,
#  provided that the above copyright notice appear in all copies and
#  that both that copyright notice and this permission notice appear in
#  supporting documentation, and that the name of Red Hat not be used in
#  advertising or publicity pertaining to distribution of the software
#  without specific, written prior permission.  Red Hat makes no
#  representations about the suitability of this software for any
#  purpose.  It is provided "as is" without express or implied warranty.
# 
#  RED HAT DISCLAIMS ALL WARRANTIES WITH REGARD TO THIS SOFTWARE,
#  INCLUDING ALL IMPLIED WARRANTIES OF MERCHANTABILITY AND FITNESS, IN
#  NO EVENT SHALL RED HAT BE LIABLE FOR ANY SPECIAL, INDIRECT OR
#  CONSEQUENTIAL DAMAGES OR ANY DAMAGES WHATSOEVER RESULTING FROM LOSS
#  OF USE, DATA OR PROFITS, WHETHER IN AN ACTION OF CONTRACT, NEGLIGENCE
#  OR OTHER TORTIOUS ACTION, ARISING OUT OF OR IN CONNECTION WITH THE
#  USE OR PERFORMANCE OF THIS SOFTWARE.
#
#  Process this file with autoconf to create configure.

SUBDIRS = man sgml specs

dist_doc_DATA = MAINTAINERS

MAINTAINERCLEANFILES = ChangeLog INSTALL
EXTRA_DIST = \
	misc/xlogo.epsi \
	misc/xlogo.svg \
	registry \
	specs/BDF/bdf.ms \
	specs/BDF/fig1.ps \
	specs/BDF/fig2.ps \
	specs/RX/RX.mif \
	specs/SIAddresses/hostname.txt \
	specs/SIAddresses/IPv6.txt \
	specs/SIAddresses/localuser.txt \
	specs/SIAddresses/README \
	specs/specindex.html \
	specs/Xext/AppGroup.mif \
	specs/Xext/lbxalg.mif \
	specs/Xext/lbx.book \
	specs/Xext/lbx.mif \
	specs/Xext/xtest1.info \
	specs/Xext/xtest1.mm \
	specs/XKB/Proto/dflttrns.fm5 \
	specs/XKB/Proto/encoding.fm5 \
	specs/XKB/Proto/keysyms.fm5 \
	specs/XKB/Proto/protocol.fm5 \
	specs/XKB/Proto/prototoc.doc \
	specs/XKB/Proto/title.fm5 \
	specs/XKB/Proto/types.fm5 \
	specs/XKB/Proto/XKBproto.book \
	specs/XKB/XKBlib/allchaps.fm5 \
	specs/XKB/XKBlib/allchaps.ix \
	specs/XKB/XKBlib/allchaps.lof \
	specs/XKB/XKBlib/allchaps.lot \
	specs/XKB/XKBlib/allchaps.ps \
	specs/XKB/XKBlib/allchaps.toc \
	specs/XKB/XKBlib/fonts.fm5 \
	specs/XKB/XKBlib/title.fm5 \
	specs/XKB/XKBlib/XKBlib.book \
	specs/Xserver/analysis.xml \
	specs/Xserver/appgroup.xml \
	specs/Xserver/secint.xml \
	util/block.awk \
	util/fixindex.awk \
	util/indexmacros.t \
	util/macros.t


.PHONY: ChangeLog INSTALL

INSTALL:
	$(INSTALL_CMD)

ChangeLog:
	$(CHANGELOG_CMD)

dist-hook: ChangeLog INSTALL
