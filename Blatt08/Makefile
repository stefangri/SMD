all: blatt08_nitschke_grisard.pdf

blatt08_nitschke_grisard.pdf: blatt08_nitschke_grisard.ipynb
	jupyter nbconvert --to notebook --execute blatt08_nitschke_grisard.ipynb --output blatt08_nitschke_grisard.ipynb
	ipython nbconvert --to pdf blatt08_nitschke_grisard.ipynb
	jupyter nbconvert --ClearOutputPreprocessor.enabled=True --inplace blatt08_nitschke_grisard.ipynb

commit: blatt08_nitschke_grisard.ipynb
	jupyter nbconvert --ClearOutputPreprocessor.enabled=True --inplace blatt08_nitschke_grisard.ipynb
	git add --all
	git commit

clearoutput:
	jupyter nbconvert --ClearOutputPreprocessor.enabled=True --inplace blatt08_nitschke_grisard.ipynb





clean:
	rm -rf blatt08_nitschke_grisard.pdf

.PHONY: clean all
