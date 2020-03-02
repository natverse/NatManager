
<!-- README.md is generated from README.Rmd. Please edit that file -->

# natmanager

<!-- badges: start -->

[![natmanager](https://img.shields.io/badge/natmanager-Part%20of%20the%20natverse-a241b6)](https://natverse.github.io)
[![Docs](https://img.shields.io/badge/docs-100%25-brightgreen.svg)](https://natverse.github.io/natmanager/reference/)
[![Travis build
status](https://travis-ci.org/natverse/natmanager.svg?branch=master)](https://travis-ci.org/natverse/natmanager)
<!-- badges: end -->

The goal of natmanager is to streamline installation of packages from
the natverse (NeuroAnatomy Toolbox) suite of R packages for
computational neuroanatomy. See <http://natverse.org/install/> for the
full details.

``` r
install.packages("natmanager")

# install core packages to try out the core natverse
natmanager::install('core')

# Full "batteries included" installation with all packages
# You need a GitHub account and personal access token (PAT) for this
natmanager::install('natverse')
```
