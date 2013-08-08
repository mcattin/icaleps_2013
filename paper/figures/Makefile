SVG=$(wildcard *.svg)
PDF=$(SVG:.svg=.pdf)
EPS=$(SVG:.svg=.eps)

.PHONY: all
all: $(PDF) $(EPS)

%.pdf : %.svg
	inkscape --without-gui $< -A $@

%.eps : %.svg
	inkscape --without-gui $< -E $@

clean:
	rm -f $(PDF)
	rm -f $(EPS)

show:
	$(info all svg: $(SVG))
	$(info all pdf: $(PDF))
	$(info all eps: $(EPS))



