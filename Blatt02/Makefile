all: blatt02_nitschke_grisard.pdf

blatt02_nitschke_grisard.pdf: blatt02_nitschke_grisard.ipynb 
	jupyter nbconvert --to notebook --execute blatt02_nitschke_grisard.ipynb --output blatt02_nitschke_grisard.ipynb
	ipython nbconvert --to pdf blatt02_nitschke_grisard.ipynb
	jupyter nbconvert --ClearOutputPreprocessor.enabled=True --inplace blatt02_nitschke_grisard.ipynb

commit: blatt02_nitschke_grisard.ipynb
	jupyter nbconvert --ClearOutputPreprocessor.enabled=True --inplace blatt02_nitschke_grisard.ipynb
	git add --all
	git commit 

clearoutput: 
	jupyter nbconvert --ClearOutputPreprocessor.enabled=True --inplace blatt02_nitschke_grisard.ipynb





clean:
	rm -rf blatt02_nitschke_grisard.pdf

.PHONY: clean all 