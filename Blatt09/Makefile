all: blatt09_nitschke_grisard.pdf

blatt09_nitschke_grisard.pdf: notebook_09.pdf
	pdfunite notebook_09.pdf scans/aufgabe_26.pdf scans/aufgabe_27.pdf blatt09_nitschke_grisard.pdf

notebook_09.pdf: notebook_09.ipynb
	jupyter nbconvert --to notebook --execute notebook_09.ipynb --output notebook_09.ipynb
	jupyter nbconvert --to pdf notebook_09.ipynb
	jupyter nbconvert --ClearOutputPreprocessor.enabled=True --inplace notebook_09.ipynb

commit: notebook_09.ipynb
	jupyter nbconvert --ClearOutputPreprocessor.enabled=True --inplace notebook_09.ipynb
	git add --all
	git commit

clearoutput:
	jupyter nbconvert --ClearOutputPreprocessor.enabled=True --inplace notebook_09.ipynb





clean:
	rm -rf blatt09_nitschke_grisard.pdf

.PHONY: clean all
