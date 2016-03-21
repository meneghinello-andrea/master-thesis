BIBLIOGRAPHY_COMPILER   = bibtex
GLOSSARY_COMPILER       = makeglossaries
REPORT_COMPILER         = pdflatex

SETTINGS                = databases/acronym.tex \
                          databases/bibliography.bib \
                          databases/glossary.tex

FRONTESPIECE            = frontispiece.pdf

PUBLISH_NAME            = Meneghinello.pdf

REPORT_FILE_NAME        = thesis

REPORT_CHAPTERS         = chapters/background/main.tex \
						  chapters/background/sections/use-cases.tex \
						  chapters/background/sections/cloud.tex \
						  chapters/background/sections/paas.tex \
						  chapters/background/sections/virtualization.tex \
						  chapters/background/sections/docker.tex \
						  chapters/background/sections/platform.tex \
						  chapters/background/sections/definition.tex \
						  chapters/elasticity/main.tex \
						  chapters/elasticity/sections/introduction.tex \
						  chapters/elasticity/sections/requirements.tex \
						  chapters/elasticity/sections/multi-tenancy.tex \
						  chapters/elasticity/sections/objective.tex 

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
