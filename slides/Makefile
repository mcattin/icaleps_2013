all : WECOCB01_talk.pdf

.PHONY : all clean

WECOCB01_talk.pdf : WECOCB01_talk.tex
#	pdflatex $^
#	pdflatex $^

#	latex $^
# 	bibtex
	latex $^
	latex $^
	dvips -j0 WECOCB01_talk
	ps2pdf  -dPDFX -dEmbedAllFonts=true -dSubsetFonts=true -dEPSCrop=true WECOCB01_talk.ps


clean :
	rm -f *.ps *.pdf *.dat *.log *.out *.aux *.dvi *~

show : WECOCB01_talk.pdf
	evince $^ &