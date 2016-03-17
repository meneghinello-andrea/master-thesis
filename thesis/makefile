BIBLIOGRAPHY_COMPILER   = bibtex
GLOSSARY_COMPILER       = makeglossaries
REPORT_COMPILER         = pdflatex

SETTINGS                = databases/acronym.tex \
                          databases/bibliography.bib \
                          databases/glossary.tex

FRONTESPIECE            = frontispiece.pdf

PUBLISH_NAME            = Meneghinello.pdf

REPORT_FILE_NAME        = thesis

REPORT_CHAPTERS         = chapters/problem/main.tex \
						  chapters/problem/sections/use-cases.tex \
						  chapters/problem/sections/cloud.tex \
						  chapters/problem/sections/paas.tex \
						  chapters/problem/sections/docker.tex \
						  chapters/problem/sections/platform.tex \
						  chapters/problem/sections/problem.tex \
						  chapters/problem/sections/summary.tex

.PHONY: clean compile publish

compile: $(SETTINGS) $(REPORT_CHAPTERS) $(REPORT_FILE_NAME).tex
	@$(REPORT_COMPILER) frontispiece/frontispiece.tex
	@$(REPORT_COMPILER) frontispiece-frn.tex
	@$(REPORT_COMPILER) frontispiece/frontispiece.tex
	@$(REPORT_COMPILER) $(REPORT_FILE_NAME).tex
	@$(GLOSSARY_COMPILER) $(REPORT_FILE_NAME)
	@$(BIBLIOGRAPHY_COMPILER) $(REPORT_FILE_NAME)
	@$(REPORT_COMPILER) $(REPORT_FILE_NAME).tex
	@$(REPORT_COMPILER) $(REPORT_FILE_NAME).tex

publish: compile
	mv $(REPORT_FILE_NAME).pdf $(PUBLISH_NAME)

clean:
	@rm -f *.aux
	@rm -f *.bib
	@rm -f *.bbl
	@rm -f *.blg
	@rm -f *.glg
	@rm -f *.glo
	@rm -f *.gls
	@rm -f *.ist
	@rm -f *.lof
	@rm -f *.log
	@rm -f *.lot
	@rm -f *.out
	@rm -f *.pdf
	@rm -f *-frn.tex
	@rm -f *.toc
	@rm -f *.xml
