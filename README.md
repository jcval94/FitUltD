
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
#> Package 'mclust' version 5.4.5
#> Type 'citation("mclust")' for citing this R package in publications.
#random Variable
RV<-c(rnorm(73,189,12),rweibull(82,401,87),rgamma(90,40,19))
set.seed(31109)
FIT1<-FDistUlt(RV, plot=TRUE, subplot = TRUE)
```

What is special about using `README.Rmd` instead of just `README.md`?
You can include R chunks like so:

``` r
FIT1[[3]]
#>                  Distribution Dist_Prop    Dist    AD_p.v    KS_p.v
#> AD8  weibull(18.969, 195.426) 0.2979592 weibull 0.8569332 0.9557278
#> AD81   weibull(454.9, 87.023) 0.3346939 weibull 0.9415304 0.9616317
#> AD6       lnorm(0.741, 0.145) 0.3673469   lnorm 0.9540176 0.8587172
#>        estimate1   estimate2 estimateLL1 estimateLL2 method     PV_S
#> AD8   18.9686456 195.4260896           0           1    mge 1.812661
#> AD81 454.8996478  87.0229602           0           1    mge 1.903162
#> AD6    0.7408106   0.1446825           0           1    mge 1.812735
```

You’ll still need to render `README.Rmd` regularly, to keep `README.md`
up-to-date.

You can also embed plots, for example:

<img src="man/figures/README-pressure-1.png" width="100%" />

<img src="man/figures/README-plots-mult-1.png" width="100%" />
