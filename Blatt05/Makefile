all: blatt05_nitschke_grisard.pdf

blatt05_nitschke_grisard.pdf: blatt05_nitschke_grisard.ipynb
	jupyter nbconvert --to notebook --execute blatt05_nitschke_grisard.ipynb --output blatt05_nitschke_grisard.ipynb
	ipython nbconvert --to pdf blatt05_nitschke_grisard.ipynb
	jupyter nbconvert --ClearOutputPreprocessor.enabled=True --inplace blatt05_nitschke_grisard.ipynb

commit: blatt05_nitschke_grisard.ipynb
	jupyter nbconvert --ClearOutputPreprocessor.enabled=True --inplace blatt05_nitschke_grisard.ipynb
	git add --all
	git commit

clearoutput:
	jupyter nbconvert --ClearOutputPreprocessor.enabled=True --inplace blatt05_nitschke_grisard.ipynb





clean:
	rm -rf blatt05_nitschke_grisard.pdf

.PHONY: clean all
