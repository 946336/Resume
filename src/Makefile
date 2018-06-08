
.PHONY:
all:
	pdflatex resume.tex
	sed 's/\\href{.*}{\([^}]*\)}/\1/g' resume.tex > resume-nolink.tex
	pdflatex resume-nolink.tex
	cp resume.pdf resume-nolink.pdf ..

.PHONY:
clean:
	rm -rf resume.log resume-nolink.log

.PHONY:
remove:
	rm -rf resume.{log,pdf} resume-nolink.{log,pdf}
	rm -rf ../resume.pdf ../resume-nolink.pdf

