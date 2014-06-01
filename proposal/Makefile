main = scientific
bib = referencias
latex = pdflatex

all: $(main).pdf

$(main).pdf: $(main).tex $(bib).bib 1titulo.tex 2investigadores.tex 3equipo.tex
	pdflatex $(main).tex
	bibtex $(main)
	pdflatex $(main).tex
	pdflatex $(main).tex

clean:
	rm -f $(main).bbl $(main).aux $(main).pdf $(main).log