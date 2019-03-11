# ai-word-embedding
Lecture prepared for the AI seminar.

# TeX installation

```
sudo apt install texlive-full
```

Then install (optionally) editor:
```
sudo apt install texmaker
```

# Fix issue with default Beamer package

While using texlive and trying to compile ```seminar_slides.tex```
via ```pdflatex``` like:

```
pdflatex -synctex=1 -interaction=nonstopmode %.tex
```

you could probably occur the following issue:
```
! Undefined control sequence.
<argument> .../enumerate \beameritemnestingprefix 
body end
l.11 \end{frame}
```

This is described [here](https://github.com/josephwright/beamer/commit/13c02e2f3dd19e0f731af105ea0ffeb9a8f01a5f),
so if you just want to make it work either:
- Update package
- Apply patch manually from [this link](https://github.com/josephwright/beamer/commit/13c02e2f3dd19e0f731af105ea0ffeb9a8f01a5f) via editing ```/usr/share/texlive/texmf-dist/tex/latex/beamer/beamerbasecompatibility.sty```

