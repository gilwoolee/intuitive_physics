
### Makefile for paper ###

NAME = intuitive_physics
UNAME = $(shell uname -s)


build:
	-rm -f *.aux *.bbl *.log *.blg *.out *.sta
	@echo Building $(NAME).tex
	pdflatex $(NAME).tex
	bibtex $(NAME)
	pdflatex $(NAME).tex
	pdflatex $(NAME).tex
	-rm -f *.aux *.bbl *.log *.blg *.out

ifeq ($(UNAME),Linux)
	@echo Linux: open pdf with evince
	evince $(NAME).pdf &
endif
ifeq ($(UNAME),Darwin)
	@echo OSX: open pdf with preview
	open $(NAME).pdf &
endif


clean:
	-rm -f *.aux *.bbl *.log *.blg *.out *.gz $(NAME).pdf
