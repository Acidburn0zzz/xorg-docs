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

x11doc_DATA = proto.pdf proto.idx.pdf
if HAVE_PDFTK
x11doc_DATA += x11.pdf
endif

x11.pdf: proto.pdf proto.idx.pdf
	$(PDFTK) proto.pdf proto.idx.pdf cat output $@

proto.pdf index.raw: $(SRCS)
	$(TBL) $^ | $(EQN) | $(TROFF) $(MSMACROS) 2> index.raw | $(PS2PDF) - proto.pdf

index.pageno: index.raw
	tail -1 $< > $@

index.troff: index.pageno $(UTIL)/block.awk $(UTIL)/fixindex.awk
	grep -v '^.pn ' index.raw | sort -f -t: +1 -3 +0n -1n | awk -f $(UTIL)/fixindex.awk | awk -f $(UTIL)/block.awk > index.troff

proto.idx.pdf: $(ISRCS) index.troff
	cat $^ | $(TROFF) -me | $(PS2PDF) - proto.idx.pdf

CLEANFILES = proto.pdf proto.idx.pdf x11.pdf index.raw index.pageno index.troff
