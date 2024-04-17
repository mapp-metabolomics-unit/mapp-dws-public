---
id: 48173l5udd340kw1a4v9tuv
title: Report Template
desc: ''
updated: 1713164913181
created: 1669800331916
---


Here we will gather keep some info, ressources and links for (metabolomics) data analysis reports.

Indeed the Dendron webpages and markdown are extremelly usefull and have been used up to now for reports. However the plain and simple pdf export is crucially lacking.

These should be possible to consult as : 

- html
- pdf
- raw format (.txt .md etc.)

A priori Rmarkdown format looks interesting for reports specifically and maybe a bit more flexible than the Jupyter notebooksbut we will check in both directions
Both are language agnostic but Jupyter might support a bit more of them.


# Rmarkdown


## Plus 
- easily support and handles .bib and bibliography lib
## Minus

## Ressources
Some ressources and links

### The Definitive Rmarkdown guide
https://bookdown.org/yihui/rmarkdown/


https://arshren.medium.com/a-high-quality-reports-using-r-markdown-76fdaba3c7b6

https://github.com/PJDeSutter/Method-Validation


https://github.com/REditorSupport/vscode-R



# Jupyter

## Plus

## Minus


## Automated reports with Jupyter Notebooks (using Jupytext and Papermill)

https://medium.com/capital-fund-management/automated-reports-with-jupyter-notebooks-using-jupytext-and-papermill-619e60c37330


# Snippets

    {
        "key": "alt+cmd+i alt+cmd+n",
        "command": "editor.action.insertSnippet",
        "when": "editorTextFocus",
        "args": {
            "snippet": "```{r $1, echo=FALSE, fig.cap=\"$2\", out.width = '90%'}\nknitr::include_graphics(file.path(params$$paths$$relative, \"docs\", params$$mapp_project, params$$mapp_batch, \"results\", \"img\", \"$1\"))\n```\n"
        }
    },

    