complete:
	rm -rf ./latex_files &&\
	mkdir -p ./latex_files &&\
	Rscript -e 'Sys.setenv(RSTUDIO_PANDOC="/usr/lib/rstudio/bin/pandoc"); rmarkdown::render(input = "cv-maus-complete.Rmd", output_file = "./latex_files/cv-maus-complete.tex"); readr::write_lines(stringr::str_replace_all(readr::read_lines("./latex_files/cv-maus-complete.tex"), "Maus, V.", "\\\\textbf{Maus, V}."), "./latex_files/cv-maus-complete.tex");' &&\
	pdflatex -output-directory=./latex_files ./latex_files/cv-maus-complete.tex &&\
	cp ./latex_files/cv-maus-complete.pdf ./../assets/cv/ &&\
	echo "All done!"
