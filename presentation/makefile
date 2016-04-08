DOCUMENT_COMPILER  = pdflatex

FRAMES             = frames/frontespiece.tex

SETTINGS           = settings/preamble.tex

PUB_NAME           = slide
DCM_NAME           = master

.PHONY: clean compile publish

compile: $(SETTINGS) $(FRAMES) $(DCM_NAME).tex
	@$(DOCUMENT_COMPILER) $(DCM_NAME).tex
	@$(DOCUMENT_COMPILER) $(DCM_NAME).tex

clean:
	@rm -f *.aux
	@rm -f *.log
	@rm -f *.nav
	@rm -f *.out
	@rm -f *.pdf
	@rm -f *.snm
	@rm -f *.toc

publish: compile $(DCM_NAME).pdf
	@mv $(DCM_NAME).pdf $(PUB_NAME).pdf