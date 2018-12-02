all: blatt06_nitschke_grisard.pdf

blatt06_nitschke_grisard.pdf: blatt06_nitschke_grisard.ipynb
	jupyter nbconvert --to notebook --execute blatt06_nitschke_grisard.ipynb --output blatt06_nitschke_grisard.ipynb
	ipython nbconvert --to pdf blatt06_nitschke_grisard.ipynb
	jupyter nbconvert --ClearOutputPreprocessor.enabled=True --inplace blatt06_nitschke_grisard.ipynb
	pdfunite blatt06_nitschke_grisard.pdf scan.pdf abgabe.pdf

commit: blatt06_nitschke_grisard.ipynb
	jupyter nbconvert --ClearOutputPreprocessor.enabled=True --inplace blatt06_nitschke_grisard.ipynb
	git add --all
	git commit

clearoutput:
	jupyter nbconvert --ClearOutputPreprocessor.enabled=True --inplace blatt06_nitschke_grisard.ipynb





clean:
	rm -rf blatt06_nitschke_grisard.pdf

.PHONY: clean all
