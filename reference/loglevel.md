# Log-Level test for Extended Airline Models

This function performs a statistical test to determine whether data
should be transformed to logarithmic scale or kept in level (original
scale)

## Usage

``` r
loglevel(input, precision = 1e-05, deps = 1e-04)
```

## Arguments

- input:

  time series

- precision:

  Numeric value specifying the tolerance for convergence of optimization
  algorithms. Default: 1e-5.

- deps:

  Numeric scalar. Step in the computation of the numerical derivatives,
  used in the optimisation routine. Default:1e-4.

## Value

An object containing the log-level test results. First the AICc of the
model in levels and then the AICc of the model with logs

## Examples

``` r
series <- rjd3toolkit::Retail$BookStores

loglevel(series)
#> AICc_level   AICc_log 
#>   2463.671   2380.876 
```
