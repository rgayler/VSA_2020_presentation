VSA 2020 Presentation
================
Ross Gayler
2020-02-22

<!-- README.md is generated from README.Rmd. Please edit that file -->

<!-- badges: start -->

[![License: CC
BY 4.0](https://img.shields.io/badge/License-CC%20BY%204.0-lightgrey.svg)](https://creativecommons.org/licenses/by/4.0/)
<!-- [![DOI](https://zenodo.org/badge/205238383.svg)](https://zenodo.org/badge/latestdoi/205238383) -->
<!-- [![Launch Rstudio Binder](http://mybinder.org/badge_logo.svg)](https://mybinder.org/v2/gh/rgayler/scorecal_CSCC_2019/master?urlpath=rstudio) -->
<!-- badges: end -->

Create the presentation, “VSA, Analogy, and Dynamic Similarity”, to be
given at the [Workshop on Developments in Hyperdimensional Computing and
Vector Symbolic
Architectures](https://sites.google.com/view/vsaworkshop2020/home) on
2020-03-16 in Heidelberg, Germany. This event is associated with the
[8th Annual Neuro-Inspired Computational Elements (NICE)
Workshop](https://niceworkshop.org/nice-2020/).

The primary purpose of this repository is to archive the source code for
creating the presentation. The secondary purpose is to document the
process of creating and running the project, in the hope that it will
save me some time for the next presentation project.

## Project setup

This assumes starting with everything that’s on my computer right now.
Your mileage *will* vary (in particular, you may have to install a bunch
of R packages).

1.  Make sure `usethis` is installed and follow the [setup
    instructions](https://usethis.r-lib.org/articles/articles/usethis-setup.html)
    so that user name and other details are set up ready for the
    project.

2.  Create empty GitHub repo `VSA_2020_presentation` using these
    [instructions](https://happygitwithr.com/new-github-first.html#make-a-repo-on-github-2).

3.  Create a local RStudio project by cloning the GitHub repo using
    these
    [instructions](https://happygitwithr.com/new-github-first.html#new-rstudio-project-via-git-clone).

4.  Create a `figs` subdirectory of the new project to contain figures
    (which will be copied from past projects).

5.  Guard against leaking credentials to GitHub. This only needs to be
    done once per user/computer but does no harm to be repeated for each
    new project.  
    `usethis::git_vaccinate()`

6.  Activate `renv` package tracking.  
    `renv::init()`  
    This starts the project with an empty library, so all the
    infrastructure will have to be installed as it is first used. You
    will use `renv::install()` a lot, in particular, you will have to
    install `usethis` into the project.

7.  Install `usethis` to the project and mark the project as using
    `usethis` (updates the project-specific `.Rprofile`).  
    `renv::install("usethis")`  
    `usethis::use_usethis()`

8.  This presentation document requires the `binb` package to enable
    rendering the output as a PDF presentation. The document uses the
    `binb` metropolis template. This requires a variety of LaTeX tools
    and fonts to be installed, in addition to the rmarkdown and knitr
    infrastructure. See
    [eddelbuettel/binb](https://github.com/eddelbuettel/binb) for `binb`
    installation advice.
    
      - Make sure the Fira Sans and Fira Mono fonts are installed.
        (Instructions on how to [check what fonts are
        installed](https://www.cyberciti.biz/tips/quickly-list-all-available-fonts.html).
        I found it convenient to download [Fira
        Sans](https://www.fontsquirrel.com/fonts/fira-sans) and [Fira
        Mono](https://www.fontsquirrel.com/fonts/fira-mono) from [Font
        Squirrel](https://www.fontsquirrel.com). Instructions on [how to
        install fonts](https://itsfoss.com/install-fonts-ubuntu/) - for
        reasons I don’t understand, using `font-manager` didn’t work,
        whereas copying the font files to `$/.fonts` did work.)
      - The first attempt to knit the presentation may result in the
        LaTeX package manager running for **ages** while installing the
        required LaTeX infrastructure.
      - For a future project it may be worth trying to set up a
        [Docker](https://www.docker.com/) image with the fonts and LaTeX
        packages installed.

9.  Copy `README.Rmd` (this document) from a prior GitHub linked project
    and edit it to explain what this project is about and how it was set
    up. Keep this up to date as the project progresses. See [GitHub
    document](https://rmarkdown.rstudio.com/github_document_format.html)
    for instructions on the contents for this kind of README to be
    rendered on GitHub.

10. Set the license.  
    `usethis::use_ccby_license()`  
    Add the appropriate license badge from
    [lukas-h/license-badges.md](https://gist.github.com/lukas-h/2a5d00690736b4c3a7ba)
    to README.Rmd.

11. Commit, push, rinse, and repeat as the project progresses. Follow
    [these
    instructions](https://happygitwithr.com/new-github-first.html#make-local-changes-save-commit-1).

## Write presentation

1.  Copy in resources from previous projects to use as a starting point.
    
      - VSA2020\_Gayler\_abstract.pdf \# submitted extended abstract of
        presentation
      - VSA2020\_Gayler\_abstract.zip \# source code of extended
        abstract
      - Figures from old presentations

2.  Write presentation, copying figures from prior documents as needed
    
      - How to make citations in Rmarkdown:
        <https://rmarkdown.rstudio.com/authoring_bibliographies_and_citations.html#bibliographies>
      - The citation style file `apa-single-spaced.csl` came from the
        [Zotero Style
        Repository](https://www.zotero.org/styles?q=id%3Aapa-single-spaced&fields=psychology&format=author-date).

3.  Render presentation by clicking the `Knit` button in the notebook
    editor window.

4.  Insert, into the presentation, links to the published/archived
    versions of the documents.
    
      - The URL of the github is already known.
      - The presentation will be published on
        [Zenodo](https://zenodo.org). A DOI can be reserved as part of
        uploading a work in progress. See
        [here](https://instruct-eric.eu/help/other/zenodo-upload-guidelines)
        for example instructions.

## Clean up and publish

1.  Remove any documents not used in current presentation.

2.  Push the final version to github.

3.  Publish to Zenodo by clicking the “Publish” button on the upload
    page. Previous work in progress versions were “Save”d rather than
    “Publish”ed.
