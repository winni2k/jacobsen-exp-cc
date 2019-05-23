doc: doc/doc.pdf
archive: analysis.tar.gz

doc/doc.pdf: src/doc.rmd
	Rscript -e "rmarkdown::render('$<')"
	mkdir -p doc
	mv src/doc.pdf $@

analysis.tar.gz:
	git ls-tree -r master --name-only | xargs tar -czf $@
