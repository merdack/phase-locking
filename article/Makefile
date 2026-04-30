LATEXMK ?= latexmk
MAIN := main
OUTDIR := build

.PHONY: all clean distclean

all:
	$(LATEXMK) -pdf -interaction=nonstopmode -halt-on-error -outdir=$(OUTDIR) $(MAIN).tex

clean:
	$(LATEXMK) -c -outdir=$(OUTDIR) $(MAIN).tex

distclean:
	$(LATEXMK) -C -outdir=$(OUTDIR) $(MAIN).tex
