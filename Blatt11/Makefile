all: blatt11_nitschke_grisard.pdf

blatt11_nitschke_grisard.pdf: notebook_11.pdf
	pdfunite notebook_11.pdf scans/blatt11_nitschke_grisard_zusatz.pdf blatt11_nitschke_grisard.pdf

notebook_11.pdf: notebook_11.ipynb
	jupyter nbconvert --to notebook --execute notebook_11.ipynb --output notebook_11.ipynb
	jupyter nbconvert --to pdf notebook_11.ipynb
	jupyter nbconvert --ClearOutputPreprocessor.enabled=True --inplace notebook_11.ipynb

commit: notebook_11.ipynb
	jupyter nbconvert --ClearOutputPreprocessor.enabled=True --inplace notebook_11.ipynb
	git add --all
	git commit

clearoutput:
	jupyter nbconvert --ClearOutputPreprocessor.enabled=True --inplace notebook_11.ipynb





clean:
	rm -rf blatt11_nitschke_grisard.pdf
	rm -rf notebook_11.pdf

.PHONY: clean all
