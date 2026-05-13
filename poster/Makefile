MAIN = poster

.PHONY: all clean

all:
	latexmk -C
	latexmk -lualatex -bibtex -shell-escape -interaction=nonstopmode $(MAIN).tex
	@test -f $(MAIN).pdf || (echo "ERROR: PDF not produced"; exit 1)
	@echo "Build successful: $(MAIN).pdf"

clean:
	latexmk -C
	rm -f *.nav *.snm
