all: blatt_11_nitschke_grisard.pdf

blatt_11_nitschke_grisard.pdf: blatt_11_nitschke_grisard.ipynb
	jupyter nbconvert --to notebook --execute blatt_11_nitschke_grisard.ipynb --ExecutePreprocessor.timeout=1100 --output blatt_11_nitschke_grisard.ipynb
	jupyter nbconvert --to pdf blatt_11_nitschke_grisard.ipynb
	jupyter nbconvert --ClearOutputPreprocessor.enabled=True --inplace blatt_11_nitschke_grisard.ipynb

commit: blatt_11_nitschke_grisard.ipynb
	jupyter nbconvert --ClearOutputPreprocessor.enabled=True --inplace blatt_11_nitschke_grisard.ipynb
	git add --all
	git commit

clearoutput:
	jupyter nbconvert --ClearOutputPreprocessor.enabled=True --inplace blatt_11_nitschke_grisard.ipynb





clean:
	rm -rf blatt11_nitschke_grisard.pdf

.PHONY: clean all
