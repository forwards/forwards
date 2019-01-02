
<!-- README.md is generated from README.Rmd. Please edit that file -->

# forwards

[![Travis-CI Build
Status](https://travis-ci.org/forwards/forwards.svg?branch=master)](https://travis-ci.org/forwards/forwards)

The **forwards** package provides anonymized data from surveys conducted
by [Forwards](https://forwards.github.io/), the R Foundation taskforce on
women and other under-represented groups.

## Installation

You can install forwards from GitHub with:

``` r
# install.packages("devtools")
devtools::install_github("forwards/forwards")
```

## Usage

The package currently contains a single dataset, `useR2016`, with
anonymized results from a survey of participants at the
[useR\! 2016](https://www.r-project.org/useR-2016/) conference. The questions and form
of responses are described in the help file (`?useR2016`).

The dataset is lazy loaded, so after loading the **forwards** package,
the `useR2016` data frame is available for use. For example the
following code cross-tabulates respondents’ age and length of time using
R:

``` r
library(forwards)
xtabs(~ Q3 + Q11, data = useR2016)
#>              Q11
#> Q3            < 2 years 2-5 years 5-10 years > 10 years
#>   > 35               22        27         54         92
#>   35 or under        45        80         72         20
```

## Code of Conduct

Please note that this package is released with a [Contributor Code of
Conduct](CONDUCT.md). By participating in this project you agree to
abide by its terms.
