
<!-- README.md is generated from README.Rmd. Please edit that file -->

# Riex

<!-- badges: start -->

<!-- badges: end -->

The main goal of Riex is to efficiently retrieve Financial and Market
data using IEX Cloud API. In addition, provide robust tool to:

  - Enable data analysis and visualization
  - Monitor Account usage and alerts

Please make sure to review and acknowledge [IEX Terms of
Use](https://iexcloud.io/terms/) before using Riex.

Effective June 1st, 2019, Subscription will be required to access third
party data.

For Subscriptions details, visit [IEX - Flexible, scalable
pricing](https://iexcloud.io/pricing/).

  - Multiple tiers are available to users depending on tehir
    requirements with capability to upgrade
  - Usage is measured based on message counts which depends on API Call
    and associated weight
  - Example [Company - API Call](https://iexcloud.io/docs/api/#company)
    has a weight of 1 for each Symbol

Additional details about usage calculations available in [Data Weight -
section](https://iexcloud.io/docs/api/#authentication) Bbest practice
about storing and sharing [Private & Publice Secret
Key](https://iexcloud.io/docs/api/#authentication)

## Installation

You can install the released version of Riex from
[CRAN](https://CRAN.R-project.org) with:

``` r
install.packages("Riex")
```

## Examples

This is a basic example which shows you how to retrieve Company info via
IEX Cloud API: iex.company(x, iex\_sk) requires 2 values 1. x : A valid
IEX Stock Symbol 2. iex\_sk : IEX Cloud API Scret Key. It is availabe to
use via Accunt Console

Keep your secret token safe. Your secret token can make any API call on
behalf of your account, including changes that may impact billing such
as enabling pay-as-you-go charges

``` r
#Load Riex Package
library(Riex)
#> Loading required package: xts
#> Loading required package: zoo
#> 
#> Attaching package: 'zoo'
#> The following objects are masked from 'package:base':
#> 
#>     as.Date, as.Date.numeric
#> Loading required package: TTR
#> Loading required package: tidyr
#> Loading required package: tibble
sk <- "sk_8ad348ad64414ddf8874dfc8752a0b22" 
x <- "TSLA"
TSLA_Co <- iex.company(x, sk)
#> [1] "Stock Info is available in IEX"
TSLA_Co
#> # A tibble: 1 x 11
#>   symbol companyName exchange industry website description CEO  
#>   <chr>  <chr>       <chr>    <chr>    <chr>   <chr>       <chr>
#> 1 TSLA   Tesla, Inc. NASDAQ   Motor V~ http:/~ Designs an~ Elon~
#> # ... with 4 more variables: securityName <chr>, issueType <chr>,
#> #   sector <chr>, employees <dbl>
```

``` r
#library(Riex)
## basic example code
```

What is special about using `README.Rmd` instead of just `README.md`?
You can include R chunks like so:

``` r
summary(cars)
#>      speed           dist       
#>  Min.   : 4.0   Min.   :  2.00  
#>  1st Qu.:12.0   1st Qu.: 26.00  
#>  Median :15.0   Median : 36.00  
#>  Mean   :15.4   Mean   : 42.98  
#>  3rd Qu.:19.0   3rd Qu.: 56.00  
#>  Max.   :25.0   Max.   :120.00
```

You’ll still need to render `README.Rmd` regularly, to keep `README.md`
up-to-date.

You can also embed plots, for example:

<img src="man/figures/README-pressure-1.png" width="100%" />

In that case, don’t forget to commit and push the resulting figure
files, so they display on GitHub\!
