all: blatt03_nitschke_grisard.pdf

blatt03_nitschke_grisard.pdf: blatt03_nitschke_grisard.ipynb
	jupyter nbconvert --to notebook --execute blatt03_nitschke_grisard.ipynb --output blatt03_nitschke_grisard.ipynb
	ipython nbconvert --to pdf blatt03_nitschke_grisard.ipynb
	jupyter nbconvert --ClearOutputPreprocessor.enabled=True --inplace blatt03_nitschke_grisard.ipynb

commit: blatt03_nitschke_grisard.ipynb
	jupyter nbconvert --ClearOutputPreprocessor.enabled=True --inplace blatt03_nitschke_grisard.ipynb
	git add --all
	git commit

clearoutput:
	jupyter nbconvert --ClearOutputPreprocessor.enabled=True --inplace blatt03_nitschke_grisard.ipynb





clean:
	rm -rf blatt03_nitschke_grisard.pdf

.PHONY: clean all
