# Curriculum Vitae

Version history and audit trail for Stefano Grancini's academic CV.

## Where the CV lives

| | |
|---|---|
| **Authoritative latest version** | <https://sgrancini.github.io/cv/cv.pdf> |
| Landing page | <https://sgrancini.github.io/cv/> |

Circulate `https://sgrancini.github.io/cv/cv.pdf` everywhere: on the website, in
emails, in application materials and inside the CV itself. It is served by GitHub
Pages from `cv.pdf` on the `main` branch of this repository.

`cv.pdf` is always the latest approved version. There are no dated filenames.
GitHub Pages lets browsers cache files for up to ten minutes, so a reader who opened
the link just before an update may need to reload.

## Source of the CV

This repository holds no editable source. The published PDF is whichever file
Stefano selects by hand in the publisher's file picker (normally a PDF downloaded
from Overleaf into `Job Market/Package/Official Documents/CV/`). That file is
never modified.

## Publish a new version

Double-click:

    /Users/stefanograncini/Desktop/WORK/Job Market/cv/Publish CV.command

Pick the PDF, read the summary it prints (path, filename, pages, size, SHA-256,
and how it differs from what is live and from every synchronized copy), then type
`y`. Nothing changes unless you confirm.

The implementation lives outside this repository, in
`Job Market/.cv-publisher/publish_cv.sh` (see its `README.md`). Do not edit
`cv.pdf` or the `Last updated` line of `index.html` by hand; the publisher owns
both and commits only those two files.

## Recover a previous version

Every publication is one commit named `Update CV — YYYY-MM-DD`.

    git log --oneline -- cv.pdf                   # list versions
    git show <commit>:cv.pdf > CV_<commit>.pdf    # extract one
