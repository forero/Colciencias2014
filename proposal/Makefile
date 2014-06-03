main = main
bib = referencias
latex = pdflatex
final = ProyectoCiencias_ForeroRomero
anexo_datos = anexos/Anexo5_DatosPersonales_Ciencias
anexo_letter = anexos/LetterCOLCIENCIAS
anexo3 = anexos/Anexo3_ProyectosActivosCiencias_Forero.pdf

all: $(final).pdf

$(final).pdf: $(main).pdf $(anexo_datos)_Cahn.pdf $(anexo_letter)_Cahn.pdf $(anexo_datos)_Park.pdf $(anexo_letter)_Park.pdf $(anexo_datos)_Gottloeber.pdf $(anexo_letter)_Gottloeber.pdf $(anexo3)
	pdftk $(main).pdf $(anexo3) $(anexo_letter)_Cahn.pdf $(anexo_letter)_Park.pdf $(anexo_letter)_Gottloeber.pdf $(anexo_datos)_Cahn.pdf $(anexo_datos)_Park.pdf $(anexo_datos)_Gottloeber.pdf $(anexo_datos)_Forero.pdf $(anexo_datos)_Gomez.pdf cat output $(final).pdf

$(main).pdf: $(main).tex $(bib).bib 1titulo.tex 2investigadores.tex 3equipo.tex 4antecedentes.tex 5tematica.tex 6resumenejecutivo.tex 7palabrasclave.tex 8planteamientoproblema.tex 9justificacion.tex 10marco.tex 11estadodelarte.tex 12objetivos.tex 13metodologia.tex 14resultados.tex 15productos.tex 16trayectoria.tex 17evaluadores.tex 18cronograma.tex 19impactoambiental.tex 20presupuesto.tex referencias.bib
	pdflatex $(main).tex
	bibtex $(main)
	pdflatex $(main).tex
	pdflatex $(main).tex

zip: 
	zip proyecto_ciencias_ForeroRomero.zip $(final).pdf *.docx 

view: 
	open $(final).pdf

clean:
	rm -f $(main).bbl $(main).aux $(main).pdf $(main).log *~