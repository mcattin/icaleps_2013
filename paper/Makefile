all : fmc_kit_draft.pdf

.PHONY : all clean

fmc_kit_draft.pdf : fmc_kit_draft.tex
	latex $^
# 	bibtex
	latex $^
	latex $^
	dvips -j0 fmc_kit_draft
	ps2pdf  -dPDFX -dEmbedAllFonts=true -dSubsetFonts=true -dEPSCrop=true fmc_kit_draft.ps


clean :
	rm -f *.ps *.pdf *.dat *.log *.out *.aux *.dvi  *~

show : fmc_kit_draft.pdf
	evince $^