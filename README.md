
<!-- README.md is generated from README.Rmd. Please edit that file -->

# natmanager

<!-- badges: start -->

[![natmanager](https://img.shields.io/badge/natmanager-Part%20of%20the%20natverse-a241b6)](https://natverse.github.io)
[![Docs](https://img.shields.io/badge/docs-100%25-brightgreen.svg)](https://natverse.github.io/natmanager/reference/)
[![Travis build
status](https://travis-ci.org/natverse/natmanager.svg?branch=master)](https://travis-ci.org/natverse/natmanager)
<!-- badges: end -->

The goal of natmanager is to handle the installation of all packages
inside the natverse repository.

# Prerequisites

To install this package you need to have `R` and `RStudio` installed.
The detailed instructions per operating system are given below.

### Mac OS X

1.  Install `R` from here:
    [r-installation](https://cloud.r-project.org/bin/macosx/)

2.  Install `RStudio`, from here:
    [RStudio-installation](https://rstudio.com/products/rstudio/download/#download)

3.  Start `RStudio` from Launchpad

### Windows

1.  Install `R` from here:
    [r-installation](https://cloud.r-project.org/bin/windows/base/)

2.  Install `RStudio`, for Windows from here:
    [RStudio-installation](https://rstudio.com/products/rstudio/download/#download)

3.  Start `RStudio` from Programs menu

### Linux

1.  Install `R`. For Debian/Ubuntu based systems type the following in
    the terminal:

<!-- end list -->

``` bash
sudo apt-get install libopenblas-base r-base
```

2.  Install `RStudio`, in terminal type below:

Go to the [RStudio downloads
page](https://www.rstudio.com/products/rstudio/download/#download) to
identify the latest release for your distribution. For Ubuntu 16, the
current installation procedure is as follows

``` bash
sudo apt-get install gdebi
cd ~/Downloads # or wherever you like to download things
wget https://download1.rstudio.org/desktop/xenial/amd64/rstudio-1.2.1578-amd64.deb
sudo gdebi rstudio-1.2.1578-amd64.deb
```

3.  Start `RStudio`, in terminal type below:

<!-- end list -->

``` bash
rstudio
```

# Installation

You can install the released version of natmanager from
[CRAN](https://CRAN.R-project.org) with:

``` r
install.packages("natmanager")
```

Or the development version from [GitHub](https://github.com/) with:

``` r
# install.packages("remotes")
remotes::install_github("natverse/natmanager")
```

# Usage

Once installed, you can install packages inside the natverse repository
as follows:

``` r
natmanager::install('natverse')
```

You can also look at all the repos available in the natverse
organization as follows:

``` r
natmanager::list_repo()
```

(Since you will rarely use natmanager there is probably no need to
*attach* the package)

# FAQs

1.  On using `install` function from the package to install a `natverse`
    repository, I’m getting an error like
below:

<!-- end list -->

``` r
Error: (converted from warning) package 'xx' was built under R version y.y.y
Execution halted
ERROR: lazy loading failed for package 'xx' 
```

This occurs mainly when your `R` version is lower than what the package
was built for (mainly `CRAN` packages are built with latest version). If
you are sure that it is a problem due to version, then you use like
below and retry the `install` function.

``` r
Sys.setenv("R_REMOTES_NO_ERRORS_FROM_WARNINGS"=TRUE)
```

See further discussion
[here](https://github.com/r-lib/remotes/issues/403)
