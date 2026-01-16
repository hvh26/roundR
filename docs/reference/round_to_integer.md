# Round to the nearest integer

The [`base::round()`](https://rdrr.io/r/base/Round.html) function rounds
the number `1.5` to `2` and the number `2.5` also to `2`, because of the
IEC 60559 standard. This function provides an integer rounding
alternative to [`base::round()`](https://rdrr.io/r/base/Round.html).

## Usage

``` r
round_to_integer(x)
```

## Arguments

- x:

  A numeric element or vector to round to the nearest integer

## Value

An integer element or vector

## Author

Gerko Vink <g.vink@uu.nl> and Hanne Oberman <h.i.oberman@uu.nl>

## Examples

``` r
library(dplyr)
#> 
#> Attaching package: ‘dplyr’
#> The following objects are masked from ‘package:stats’:
#> 
#>     filter, lag
#> The following objects are masked from ‘package:base’:
#> 
#>     intersect, setdiff, setequal, union
# unexpected rounding
c(0.5, 1.5, 2.5, 3.5) |> round()
#> [1] 0 2 2 4
# rounding to nearest integer
c(0.5, 1.5, 2.5, 3.5) |> round_to_integer()
#> [1] 1 2 3 4
```
