main = scientific
bib = referencias
latex = pdflatex

all: $(main).pdf

$(main).pdf: $(main).tex $(bib).bib
	pdflatex $(main).tex
	bibtex $(main)
	pdflatex $(main).tex
	pdflatex $(main).tex

clean:
	rm -f $(main).bbl $(main).aux $(main).pdf $(main).log