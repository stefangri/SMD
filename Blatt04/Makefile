all: blatt04_nitschke_grisard.pdf

blatt04_nitschke_grisard.pdf: blatt04_nitschke_grisard.ipynb
	jupyter nbconvert --to notebook --execute blatt04_nitschke_grisard.ipynb --output blatt04_nitschke_grisard.ipynb
	ipython nbconvert --to pdf blatt04_nitschke_grisard.ipynb
	jupyter nbconvert --ClearOutputPreprocessor.enabled=True --inplace blatt04_nitschke_grisard.ipynb

commit: blatt04_nitschke_grisard.ipynb
	jupyter nbconvert --ClearOutputPreprocessor.enabled=True --inplace blatt04_nitschke_grisard.ipynb
	git add --all
	git commit

clearoutput:
	jupyter nbconvert --ClearOutputPreprocessor.enabled=True --inplace blatt04_nitschke_grisard.ipynb





clean:
	rm -rf blatt04_nitschke_grisard.pdf

.PHONY: clean all
