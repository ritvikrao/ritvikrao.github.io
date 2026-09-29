# make          private CV and resume in build/, with the address and phone
#               number from personal.tex; fails if the resume exceeds 1 page
# make public   CV and resume without personal info, copied to ../files/cv.pdf
#               and ../files/resume.pdf for the site
# make clean    remove build/
#
# Public builds define \cvpublic, so cvstyle.sty never reads personal.tex.
# As a second check, `make public` refuses to copy either PDF if its build
# recorded reading personal.tex, or if it still has [TODO: ...] markers.

LATEXMK = latexmk -pdf -outdir=build -interaction=nonstopmode -halt-on-error
PUBLIC  = -usepretex='\def\cvpublic{}'

# $(call one_page,file.pdf): fail unless the PDF is exactly 1 page.
one_page = pages=$$(pdfinfo $(1) | awk '/^Pages:/ {print $$2}'); \
	if [ "$$pages" != 1 ]; then \
	  echo "error: $(1) is $$pages pages; the resume must fit on 1" >&2; exit 1; fi

# $(call safe_to_publish,name): fail if build/name.pdf read personal.tex or
# still has TODO markers.
safe_to_publish = \
	if grep -q 'personal\.tex' build/$(1).fls; then \
	  echo 'error: $(1) build read personal.tex; not copying' >&2; exit 1; fi; \
	if pdftotext build/$(1).pdf - | grep -q 'TODO'; then \
	  echo 'error: $(1).pdf still has [TODO: ...] markers; not copying' >&2; exit 1; fi

.PHONY: all private public clean
all private:
	$(LATEXMK) cv.tex resume.tex
	@$(call one_page,build/resume.pdf)

public:
	$(LATEXMK) $(PUBLIC) -jobname=cv-public cv.tex
	$(LATEXMK) $(PUBLIC) -jobname=resume-public resume.tex
	@$(call safe_to_publish,cv-public)
	@$(call safe_to_publish,resume-public)
	@$(call one_page,build/resume-public.pdf)
	cp build/cv-public.pdf ../files/cv.pdf
	cp build/resume-public.pdf ../files/resume.pdf

clean:
	rm -rf build
