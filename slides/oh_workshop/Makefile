all : oh_workshop_talk.pdf

.PHONY : all clean

oh_workshop_talk.pdf : oh_workshop_talk.tex
#	pdflatex $^
#	pdflatex $^

#	latex $^
# 	bibtex
	latex $^
	latex $^
	dvips -j0 oh_workshop_talk
	ps2pdf  -dPDFX -dEmbedAllFonts=true -dSubsetFonts=true -dEPSCrop=true oh_workshop_talk.ps


clean :
	rm -f *.ps *.pdf *.dat *.log *.out *.aux *.dvi *~ *.nav *.snm *.vrb *.toc

show : oh_workshop_talk.pdf
	evince $^ &