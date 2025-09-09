.PHONY: all cv cv-uam alareo/cv.pdf alareo/cv-ii-uam.pdf alareo/resume.pdf 

CC = xelatex
ALAREO_DIR = alareo

all: alareo/cv.pdf alareo/cv-ii-uam.pdf alareo/resume.pdf
cv: alareo/cv.pdf
cv-uam: alareo/cv-ii-uam.pdf

alareo/cv.pdf: $(ALAREO_DIR)/cv.tex
	$(CC) -output-directory=$(ALAREO_DIR) $<
	biber $(ALAREO_DIR)/cv
	$(CC) -output-directory=$(ALAREO_DIR) $<

alareo/cv-ii-uam.pdf: $(ALAREO_DIR)/cv-ii-uam.tex
	$(CC) -output-directory=$(ALAREO_DIR) $<
	biber $(ALAREO_DIR)/cv-ii-uam
	$(CC) -output-directory=$(ALAREO_DIR) $<

alareo/resume.pdf: $(ALAREO_DIR)/resume.tex
	$(CC) -output-directory=$(ALAREO_DIR) $<
	biber $(ALAREO_DIR)/resume
	$(CC) -output-directory=$(ALAREO_DIR) $<

clean:
	rm -rf $(ALAREO_DIR)/*.pdf

prereq:
	sudo apt-get update
	sudo apt-get install -y texlive-xetex texlive-latex-extra texlive-fonts-extra