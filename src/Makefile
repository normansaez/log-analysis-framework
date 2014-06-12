TEXFILES = $(wildcard *.tex)
PDFFILES = $(TEXFILES:.tex=.pdf)
PNGFILES = $(PDFFILES:.pdf=.png)

DOCNAME=9152-50

all: pdf

pdf: $(PDFFILES)

%.pdf: %.tex
	echo $(TEXFILES)
	@rubber --pdf $<
	mv *.pdf ../$(DOCNAME).pdf
clean:
	@rubber --clean $(TEXFILES:.tex=)
	@rm -fr *.aux *.toc *.bbl *.blg *.log *.pdf
distclean: clean
	@rubber --clean --pdf $(TEXFILES:.tex=)

