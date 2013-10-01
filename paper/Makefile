all : WECOCB01.pdf

.PHONY : all clean

WECOCB01.pdf : WECOCB01.tex
	latex $^
# 	bibtex
	latex $^
	latex $^
	dvips -j0 WECOCB01
	ps2pdf  -dPDFX -dEmbedAllFonts=true -dSubsetFonts=true -dEPSCrop=true WECOCB01.ps


clean :
	rm -f *.ps *.pdf *.dat *.log *.out *.aux *.dvi *~

show : WECOCB01.pdf
	evince $^ &