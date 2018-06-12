*insert the travis-ci badge here*

# lab00

Welcome to RMarkdown &amp; Pathing lab. Please note, that the RMarkdown document is contained in the `rmarkdown-examples` folder.

## Overview

Please commit your work in the `rmarkdown-example.Rmd` document within the `rmarkdown-examples` directory. Make sure to commit your _rendered_ files (e.g. `rmarkdown-example.html` or `rmarkdown-example.pdf`) into this directory as well. Please see the `rmarkdown-example.html` file.

## Files Included

### Common files

- `README.md`: a file that provides guidance as to what the assignment is and what is contained inside the repository. 
    - You are reading this file right now!
- `rmarkdown-example.Rmd` document within the `rmarkdown-examples` directory: the lab file that we will be working with this time. Generally, lab files will be named `hwXX-assign.Rmd`. 
- `.gitignore`: an optional file that _RStudio_ may generate, which prevents certain files from being **committed** into the repository as they have no value.
- `<REPO-NAME>.Rproj`: an optional file that is generated when an _RStudio_ project is created. As we are using RStudio Cloud, this file likely won't be present. For those that prefer to work inside their local _RStudio_ project, you may be prompted to commit this file into the repository.

### Infrastructure for Testing

- `.travis.yml`: provides a foundation for performing [continuous integration](https://travis-ci.com) checks, or verify that we can render/create output from your RMarkdown file. If your RMarkdown file is correct, then "Build Status" badge that should be inserted inside this README will be green and show say "build success." Otherwise, the badge will be red to indicate that a "build failure" occurred. Build failures occur if: 
    - Image files have not been committed or the path to the image file is inappropriate. _Hint:_ Use relative paths!
    - You added an additional package that was not listed in the `DESCRIPTION` file and, thus, is not available when travis tries to build the `.Rmd` file.
- `DESCRIPTION`: a file associated with _R Packages_ that indicates to **Travis** what dependencies must be installed in order to build the `.Rmd` files.
- `test/render_rmds.R`: a short _R_ script that finds all instances of the `.Rmd` files and attempts to build them! 

# Acknowledgement

The testing apparatus (e.g. `/test`) and portions of the README were based off of an example done by [Carl Boettiger](http://carlboettiger.info).

