# graduate-dissertation
Master's degree dissertation

## Configuration for Org mode
In Emacs, we should have something like this in its configuration file to be able to compile the Org's document:

```
(require 'ox-latex)
(with-eval-after-load "ox-latex"
  (add-to-list 'org-latex-classes
               '("scrreprt" "\\documentclass{scrreprt}"
                 ("\\chapter{%s}" . "\\chapter*{%s}")
                 ("\\section{%s}" . "\\section*{%s}")
                 ("\\subsection{%s}" . "\\subsection*{%s}")
                 ("\\subsubsection{%s}" . "\\subsubsection*{%s}")
                 ("\\paragraph{%s}" . "\\paragraph*{%s}"))))
```
