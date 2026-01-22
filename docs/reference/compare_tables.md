# Compare Tables for Validation

Compare Tables for Validation

## Usage

``` r
compare_tables(
  expected,
  observed,
  match_cols = c("id", "text"),
  comp_cols = NULL
)
```

## Arguments

- expected:

  the expected table

- observed:

  the observed table

- match_cols:

  which columns should be used to determine identification

- comp_cols:

  which columns should be compared for classification

## Value

a list of comparisons

## Examples

``` r
expected <- data.frame(id = 1:2, text = c("A", "B"), value = c(10, 20))
observed <- data.frame(id = 1:2, text = c("A", "B"), value = c(10, 25))
compare_tables(expected, observed)
#> $identification
#>       exp       obs  true_pos false_pos false_neg 
#>         2         2         2         0         0 
#> 
#> $classification
#> value 
#>   0.5 
#> 
#> $table
#>   id text value.exp value.obs  exp  obs true_pos false_pos false_neg
#> 1  1    A        10        10 TRUE TRUE     TRUE     FALSE     FALSE
#> 2  2    B        20        25 TRUE TRUE     TRUE     FALSE     FALSE
#> 
```
