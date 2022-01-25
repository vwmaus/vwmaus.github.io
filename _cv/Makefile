pdf:
	rm -rf ./latex_files &&\
	mkdir -p ./latex_files &&\
	Rscript -e 'Sys.setenv(RSTUDIO_PANDOC="/usr/lib/rstudio/bin/pandoc"); rmarkdown::render(input = "cv-maus-complete.Rmd", output_file = "./latex_files/cv-maus-complete.tex",  output_yaml = "output_pdf.yml"); readr::write_lines(stringr::str_replace_all(readr::read_lines("./latex_files/cv-maus-complete.tex"), "Maus, V.", "\\\\textbf{Maus, V}."), "./latex_files/cv-maus-complete.tex");' &&\
	pdflatex -output-directory=./latex_files ./latex_files/cv-maus-complete.tex &&\
	cp ./latex_files/cv-maus-complete.pdf ./../assets/cv/ &&\
	echo "All done!"

html:
	rm -rf ./latex_files &&\
	mkdir -p ./latex_files &&\
	Rscript -e 'Sys.setenv(RSTUDIO_PANDOC="/usr/lib/rstudio/bin/pandoc"); library(rmarkdown); rmarkdown::render(input = "cv-maus-complete.Rmd",  output_yaml = "output_html.yml");' &&\
	#Rscript -e 'Sys.setenv(RSTUDIO_PANDOC="/usr/lib/rstudio/bin/pandoc"); library(rmarkdown); rmarkdown::render(input = "cv-maus-complete.Rmd", output_file = "./latex_files/cv-maus-complete.html", output_dir = "./latex_files",  output_yaml = "output_html.yml");' &&\
	echo "All done!"
