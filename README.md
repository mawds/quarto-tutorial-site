# Tutorials test site using Quarto

This repo contains details of setting up a website to host tutorials using Quarto.

To start a new site:

* Install [Quarto](https://quarto.org/) on local machine
* Create a new directory and initalise a git repo
* Generate initial Quarto website: `quarto create-project --type website`
* Setup to host on Github pages:
	* `touch .nojekyll`
	* Modify  `_quarto.yml` to output to `docs`

```
project:
  type: website
  output-dir: docs
``` 

	* On Github - setup github pages: choose settings, Pages (LH sidebar), choose main as branch and docs/ as folder, save
	* Wait a few minutes - can follow progress in actions tab


The rendered site is hosted at https://mawds.github.io/quarto-tutorial-site/


## Editing the site

You will typically want to run `quarto preview` in a separate window to get a live update of changes (a local URL to see the changes will be provided).
Once you're done editing, run `quarto render` (or `quarto render --execute` to re-run all cells, rather than use the state saved in the notebook).  The rendered
site will be in `docs/`'; add this to a commit and it will be published on github pages when you push the commit.

