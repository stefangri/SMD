all: blatt10_nitschke_grisard.pdf

blatt10_nitschke_grisard.pdf: notebook_10.pdf
	pdfunite notebook_10.pdf scans/aufgabe_26.pdf scans/aufgabe_27.pdf blatt10_nitschke_grisard.pdf

notebook_10.pdf: notebook_10.ipynb
	jupyter nbconvert --to notebook --execute notebook_10.ipynb --output notebook_10.ipynb
	jupyter nbconvert --to pdf notebook_10.ipynb
	jupyter nbconvert --ClearOutputPreprocessor.enabled=True --inplace notebook_10.ipynb

commit: notebook_10.ipynb
	jupyter nbconvert --ClearOutputPreprocessor.enabled=True --inplace notebook_10.ipynb
	git add --all
	git commit

clearoutput:
	jupyter nbconvert --ClearOutputPreprocessor.enabled=True --inplace notebook_10.ipynb





clean:
	rm -rf blatt10_nitschke_grisard.pdf

.PHONY: clean all
