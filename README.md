
<!-- README.md is generated from README.Rmd. Please edit that file -->

# FitUltD

<!-- badges: start -->

<!-- badges: end -->

The goal of FitUltD is to fit data that can’t be fitted with ordinary
density functions

## Installation

You can install the released version of FitUltD from
[CRAN](https://CRAN.R-project.org) with:

install.packages(“FitUltD”)

## Example

This is a basic example which shows you how to fit a multimodal random
variable:

``` r
library(FitUltD)
#> Loading required package: mclust
#> Package 'mclust' version 5.4.3
#> Type 'citation("mclust")' for citing this R package in publications.
#random Variable
RV<-c(rnorm(73,189,12),rweibull(82,401,87),rgamma(90,40,19))

FIT1<-FDistUlt(RV, plot=TRUE, subplot = TRUE)
```

What is special about using `README.Rmd` instead of just `README.md`?
You can include R chunks like so:

``` r
FIT1[[3]]
#>                  Distribucion Prop_dist    AD_p.v    KS_p.v Chs_p.v
#> AD8  weibull(17.245, 194.365) 0.2979592 0.9396423 0.9876407       0
#> AD81 weibull(436.082, 87.016) 0.3346939 0.9632955 0.9717303       0
#> AD6        lnorm(0.732, 0.17) 0.3673469 0.9177670 0.8679283       0
```

You’ll still need to render `README.Rmd` regularly, to keep `README.md`
up-to-date.

You can also embed plots, for example:

<img src="man/figures/README-pressure-1.png" width="100%" />

<img src="man/figures/README-plots mult-1.png" width="100%" />
