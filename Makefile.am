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

SUBDIRS = man sgml specs/XProtocol
x11docdir = @X11DOCDIR@

dist_x11doc_DATA = MAINTAINERS

MAINTAINERCLEANFILES = ChangeLog INSTALL
EXTRA_DIST = \
	MAINTAINERS \
	misc/xlogo.epsi \
	registry \
	specs/BDF/bdf.ms \
	specs/BDF/fig1.ps \
	specs/BDF/fig2.ps \
	specs/CTEXT/ctext.tbl.ms \
	specs/FSProtocol/protocol.ms \
	specs/ICCCM/icccm.ms \
	specs/ICCCM/indexmacros.t \
	specs/RX/RX.mif \
	specs/saver/saver.ms \
	specs/SIAddresses/hostname.txt \
	specs/SIAddresses/IPv6.txt \
	specs/SIAddresses/localuser.txt \
	specs/SIAddresses/README \
	specs/specindex.html \
	specs/XDMCP/xdmcp.ms \
	specs/Xext/AppGroup.mif \
	specs/Xext/bigreq.ms \
	specs/Xext/buffer.ms \
	specs/Xext/dbe.tex \
	specs/Xext/DPMS.ms \
	specs/Xext/evi.ms \
	specs/Xext/lbxalg.mif \
	specs/Xext/lbx.book \
	specs/Xext/lbx.mif \
	specs/Xext/mit-shm.ms \
	specs/Xext/recordlib.ms \
	specs/Xext/record.ms \
	specs/Xext/security.tex \
	specs/Xext/shape.ms \
	specs/Xext/sync.tex \
	specs/Xext/tog-cup.ms \
	specs/Xext/xc-misc.ms \
	specs/Xext/xtest1.info \
	specs/Xext/xtest1.mm \
	specs/Xext/xtestlib.ms \
	specs/Xext/xtest.ms \
	specs/Xi/encoding.ms \
	specs/Xi/library.ms \
	specs/Xi/porting.ms \
	specs/Xi/protocol.txt \
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
	specs/XLFD/xlfd.tbl.ms \
	specs/Xserver/analysis.tex \
	specs/Xserver/appgroup.ms \
	specs/Xserver/secint.tex \
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
