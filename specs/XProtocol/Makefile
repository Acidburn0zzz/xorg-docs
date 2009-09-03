TBL = tbl
EQN = eqn
TROFF = groff -Tps
MSMACROS = -ms
UTIL = ../../util
SRCS = $(UTIL)/macros.t X11.protocol X11.keysyms X11.encoding glossary postproc
ISRCS = indexmacros.t $(UTIL)/indexmacros.t

all: x11.pdf

x11.pdf: proto.pdf proto.idx.pdf
	pdftk proto.pdf proto.idx.pdf cat output $@

proto.pdf:
	$(TBL) $(SRCS) | $(EQN) | $(TROFF) $(MSMACROS) 2> index.raw | ps2pdf - proto.pdf

proto.idx.pdf: proto.pdf
	tail -1 index.raw > index.pageno
	grep -v '^.pn ' index.raw | sort -f -t: +1 -3 +0n -1n | awk -f $(UTIL)/fixindex.awk | awk -f $(UTIL)/block.awk > index.troff
	cat $(ISRCS) index.troff | $(TROFF) -me | ps2pdf - proto.idx.pdf
	$(RM) index.troff index.pageno

clean::
	$(RM) index.raw index.troff index.pageno proto.pdf proto.idx.pdf

