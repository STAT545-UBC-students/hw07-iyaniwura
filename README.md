
<!-- README.md is generated from README.Rmd. Please edit that file -->
<!-- README.md is generated from README.Rmd. Please edit that file -->
[![Build Status](https://travis-ci.org/vincenzocoia/powers.svg?branch=master)](https://travis-ci.org/vincenzocoia/powers)

**Note**: This R package is not mean to be "serious". It's just for homework purposes.

powers
======

This is an R package that gives the power of a vector of numbers. The functions contained in this package include:

    1. `square()` function: squares a vector of numbers
    2. `reciprocal()` function: computed `1/x`, where `x` is a vector of numbers
    3. `cube()` function: raise a vector of numbers to power 3
    4. `Box_Cox()` function: compute Box-Cox transformation of a vector

Installation
------------

You can install powers from github with:

``` r
# install.packages("devtools")
devtools::install_github("STAT545-UBC-students/hw07-iyaniwura")
```

Example
-------

See the vignette for more extensive use, but here's an example:

``` r
powers::square(3)
#> [1] 9
```

``` r
powers::cube(4)
#> [1] 64
```

``` r
powers::reciprocal(5)
#> [1] 0.2
```

``` r
vec <- c(2,3,4,2)
powers::Box_Cox(vec,2)
#> [1] 1.5 4.0 7.5 1.5
```

For Developers
--------------

Use the internal `pow` function as the machinery for the front-end functions such as `square`, `cube`, and `reciprocal`. Although, the `Box_Cox` function is independent of the power function
