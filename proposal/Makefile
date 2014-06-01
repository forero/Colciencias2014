main = main
bib = referencias
latex = pdflatex

all: $(main).pdf

$(main).pdf: $(main).tex $(bib).bib 1titulo.tex 2investigadores.tex 3equipo.tex 4antecedentes.tex 5tematica.tex 6resumenejecutivo.tex 7palabrasclave.tex 8planteamientoproblema.tex 9justificacion.tex 10marco.tex 11estadodelarte.tex 12objetivos.tex 13metodologia.tex 14resultados.tex 15productos.tex 16trayectoria.tex 17evaluadores.tex 18cronograma.tex 19impactoambiental.tex 20presupuesto.tex
	pdflatex $(main).tex
	bibtex $(main)
	pdflatex $(main).tex
	pdflatex $(main).tex

clean:
	rm -f $(main).bbl $(main).aux $(main).pdf $(main).log