

# This is PMA's MAPP Metabolomics daily Open Notebook.

Today is 2024.04.15

## Todo today

### Have a look at the MAPP Metabolomics discussion forum
    - https://github.com/orgs/mapp-metabolomics-unit/discussions
###
###

## Doing

## Paused

## Done

Created the following snippet to insert img in the Report template

    {
        "key": "alt+cmd+i alt+cmd+n",
        "command": "editor.action.insertSnippet",
        "when": "editorTextFocus",
        "args": {
            "snippet": "```{r $1, echo=FALSE, fig.cap=\"$2\", out.width = '90%'}\nknitr::include_graphics(file.path(params$$paths$$relative, \"docs\", params$$mapp_project, params$$mapp_batch, \"results\", \"img\", \"$1\"))\n```\n"
        }
    },

    

## Notes

## Todo tomorrow

###
###
###


## Today I learned that

-