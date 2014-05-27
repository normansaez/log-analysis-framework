TEXFILES = $(wildcard *.tex)
PDFFILES = $(TEXFILES:.tex=.pdf)
PNGFILES = $(PDFFILES:.pdf=.png)

all: pdf

pdf: $(PDFFILES)

%.pdf: %.tex
	echo $(TEXFILES)
	@rubber --pdf $<
	mv *.pdf ../doc
clean:
	@rubber --clean $(TEXFILES:.tex=)
	@rm -fr *.aux *.toc *.bbl *.blg *.log *.pdf
distclean: clean
	@rubber --clean --pdf $(TEXFILES:.tex=)

