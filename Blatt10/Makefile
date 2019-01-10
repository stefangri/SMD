all: blatt_10_nitschke_grisard.pdf

blatt_10_nitschke_grisard.pdf: blatt_10_nitschke_grisard.ipynb
	jupyter nbconvert --to notebook --execute blatt_10_nitschke_grisard.ipynb --ExecutePreprocessor.timeout=1000 --output blatt_10_nitschke_grisard.ipynb
	jupyter nbconvert --to pdf blatt_10_nitschke_grisard.ipynb
	jupyter nbconvert --ClearOutputPreprocessor.enabled=True --inplace blatt_10_nitschke_grisard.ipynb

commit: blatt_10_nitschke_grisard.ipynb
	jupyter nbconvert --ClearOutputPreprocessor.enabled=True --inplace blatt_10_nitschke_grisard.ipynb
	git add --all
	git commit

clearoutput:
	jupyter nbconvert --ClearOutputPreprocessor.enabled=True --inplace blatt_10_nitschke_grisard.ipynb





clean:
	rm -rf blatt10_nitschke_grisard.pdf

.PHONY: clean all
