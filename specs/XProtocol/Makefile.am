x11docdir = @X11DOCDIR@/specs/XProtocol

TBL = tbl
EQN = eqn
TROFF = groff -Tps
MSMACROS = -ms
UTIL = $(top_srcdir)/util
protoSRCS = X11.protocol X11.keysyms X11.encoding glossary postproc
indexSRCS = indexmacros.t
SRCS = $(UTIL)/macros.t $(protoSRCS)
ISRCS = $(indexSRCS) $(UTIL)/indexmacros.t
EXTRA_DIST = $(indexSRCS) $(protoSRCS)

x11doc_DATA = x11.pdf proto.pdf proto.idx.pdf

x11.pdf: proto.pdf proto.idx.pdf
	pdftk proto.pdf proto.idx.pdf cat output $@

proto.pdf index.raw: $(SRCS)
	$(TBL) $^ | $(EQN) | $(TROFF) $(MSMACROS) 2> index.raw | ps2pdf - proto.pdf

index.pageno: index.raw
	tail -1 $< > $@

index.troff: index.pageno $(UTIL)/block.awk $(UTIL)/fixindex.awk
	grep -v '^.pn ' index.raw | sort -f -t: +1 -3 +0n -1n | awk -f $(UTIL)/fixindex.awk | awk -f $(UTIL)/block.awk > index.troff

proto.idx.pdf: $(ISRCS) index.troff
	cat $^ | $(TROFF) -me | ps2pdf - proto.idx.pdf

CLEANFILES = proto.pdf proto.idx.pdf x11.pdf index.raw index.pageno index.troff

