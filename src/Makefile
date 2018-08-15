
.PHONY:
all: resume resume-nolink

resume: resume.tex resume.cls
	pdflatex resume.tex

resume-nolink: resume.tex resume.cls
	sed 's/\\href{.*}{\([^}]*\)}/\1/g' resume.tex > resume-nolink.tex
	pdflatex resume-nolink.tex

.PHONY:
export: resume resume-nolink
	cp resume.pdf WesleyWei-resume.pdf
	cp resume-nolink.pdf WesleyWei-resume-nolink.pdf
	mv WesleyWei-resume.pdf WesleyWei-resume-nolink.pdf ..

.PHONY:
clean:
	rm -rf resume.{log,pdf} resume-nolink.{log,pdf}

.PHONY:
remove:
	rm -rf ../WesleyWei-resume.pdf ../WesleyWei-resume-nolink.pdf

