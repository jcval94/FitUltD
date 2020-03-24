
<!-- README.md is generated from README.Rmd. Please edit that file -->
FitUltD
=======

<!-- badges: start -->
<!-- badges: end -->
The goal of FitUltD is to fit data that can't be fitted with ordinary density functions

Installation
------------

You can install the released version of FitUltD from [CRAN](https://CRAN.R-project.org) with:

install.packages("FitUltD")

Example
-------

This is a basic example which shows you how to fit a multimodal random variable:

``` r
library(FitUltD)
#> Loading required package: mclust
#> Package 'mclust' version 5.4.5
#> Type 'citation("mclust")' for citing this R package in publications.
#Random Variable
RV <- c(rnorm(73,189,12), rweibull(82,401,87), rgamma(90,40,19))
set.seed(311093)
FIT1 <- FDistUlt(RV, plot = TRUE, subplot = TRUE)
#> Error in computing default starting values.
#> Error in computing default starting values.
#> Error in computing default starting values.
#> Error in computing default starting values.
#> Error in computing default starting values.
#> Error in computing default starting values.
#> Error in computing default starting values.
#> Error in computing default starting values.
#> Error in computing default starting values.
#> Error in computing default starting values.
#> Error in computing default starting values.
#> Error in computing default starting values.
```

One of the available options is to show the distribution functions that passed the Anderson Darling and Kolmogorov Smirnov tests, as well as their p-value and the proportion of the total distribution.

``` r
FIT1[[3]]
#>                  Distribution Dist_Prop    Dist    AD_p.v    KS_p.v  estimate1
#> AD6       lnorm(5.239, 0.051) 0.2979592   lnorm 0.5216458 0.7939035   5.238993
#> AD8  weibull(370.829, 86.974) 0.3346939 weibull 0.9858631 0.9939599 370.828837
#> AD10       norm(2.078, 0.312) 0.3673469    norm 0.8530269 0.8549550   2.077990
#>        estimate2 estimateLL1 estimateLL2 method     PV_S Obs    Lim_inf
#> AD6   0.05137778           0           1    mge 1.315549  73 168.204371
#> AD8  86.97421201           0           1    mge 1.979823  82  85.863558
#> AD10  0.31192627           0           1    mle 1.707982  90   1.390518
#>         Lim_sup
#> AD6  213.207681
#> AD8   87.399901
#> AD10   2.946422
```

By setting `plot` and `subplot` arguments as `TRUE`, is possible to visualizate each distribution which forms the most accurrate model.

Real data distribution versus fitted model.

<img src="man/figures/README-pressure-1.png" width="100%" />

Distributions that forms the fitted model.

<img src="man/figures/README-plots-mult-1.png" width="100%" />
