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

4.  Create a `past_pres` and a `figs` subdirectory of the new project
    because I anticipate using a lot past presentations and copying
    pages out of them to use as figures in the current presentation.

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
    `renv::install("usethis") usethis::use_usethis()`

8.  Copy README.Rmd (this document) from a prior GitHub linked project
    and edit it to explain what this project is about and how it was set
    up. Keep this up to date as the project progresses. See [GitHub
    document](https://rmarkdown.rstudio.com/github_document_format.html)
    for instructions on the contents for this kind of README to be
    rendered on GitHub.

9.  Set the license.  
    `usethis::use_ccby_license()`  
    Add the appropriate license badge from
    [lukas-h/license-badges.md](https://gist.github.com/lukas-h/2a5d00690736b4c3a7ba)
    to README.Rmd.

10. Commit, push, rinse, and repeat as the project progresses. Follow
    [these
    instructions](https://happygitwithr.com/new-github-first.html#make-local-changes-save-commit-1).

## Write presentation

1.  Copy in resources from previous projects to use as a starting
    point.  

<!-- end list -->

  - VSA2020\_Gayler\_abstract.pdf \# submitted extended abstract of
    presentation
  - scorecal\_CSCC\_2019 / scorecal\_CSCC\_2019.Rmd \# use as template
    for current presentation
  - scorecal\_CSCC\_2019 / by.png \# CC-BY logo
  - old presentations

<!-- end list -->

1.  Write presentation, copying figures from prior documents as needed

2.  Render presentation (how???)

## Clean up and publish

1.  Remove any documents not used in current presentation.

2.  Publish to github (how???)

3.  Publish to Zenodo ???