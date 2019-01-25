PROJ = main 
FIGS = 
FIGOUT = 
MAIN =  main.tex
SECTIONS = *.tex
APPENDICES = 
FULL = $(MAIN) $(FIGS) $(FIGOUT) $(SECTIONS) $(APPENDICES)

main.pdf : $(FULL)  *.tex
	pdflatex $(PROJ).tex

full : $(FULL)
	pdflatex $(MAIN)
	bibtex $(PROJ)
	pdflatex $(MAIN)
	pdflatex $(MAIN)

zip : $(FULL) $(PROJ).pdf Makefile
	zip $(PROJ).zip $(PROJ).pdf $(FULL) Makefile *.tex
