all: blatt07_nitschke_grisard.pdf

blatt07_nitschke_grisard.pdf: blatt07_nitschke_grisard.ipynb
	jupyter nbconvert --to notebook --execute blatt07_nitschke_grisard.ipynb --output blatt07_nitschke_grisard.ipynb
	ipython nbconvert --to pdf blatt07_nitschke_grisard.ipynb
	jupyter nbconvert --ClearOutputPreprocessor.enabled=True --inplace blatt07_nitschke_grisard.ipynb

commit: blatt07_nitschke_grisard.ipynb
	jupyter nbconvert --ClearOutputPreprocessor.enabled=True --inplace blatt07_nitschke_grisard.ipynb
	git add --all
	git commit

clearoutput:
	jupyter nbconvert --ClearOutputPreprocessor.enabled=True --inplace blatt07_nitschke_grisard.ipynb





clean:
	rm -rf blatt07_nitschke_grisard.pdf

.PHONY: clean all
