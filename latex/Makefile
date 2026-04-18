# Makefile for Agentic AI Evaluation White Paper
# Requires: pdflatex, bibtex, latexmk

.PHONY: all clean view

MAIN = main
TEX = $(MAIN).tex
PDF = $(MAIN).pdf

all: $(PDF)

$(PDF): $(TEX) references.bib sections/*.tex figures/*.tex
	latexmk -pdflatex -interaction=nonstopmode $(TEX)

clean:
	latexmk -C
	rm -f *.aux *.bbl *.blg *.log *.out *.toc *.fls *.fdb_latexmk *.synctex.gz

view: $(PDF)
	open $(PDF) 2>/dev/null || xdg-open $(PDF) 2>/dev/null || echo "Open $(PDF) manually"