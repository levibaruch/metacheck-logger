# Check Stats

Check Stats

## Usage

``` r
stats(text, ...)
```

## Arguments

- text:

  the search table (or list of paper objects)

- ...:

  arguments to pass to statcheck()

## Value

a table of statistics

## Examples

``` r
filename <- demoxml()
papers <- read(filename)
stats(papers)
#>   test_type df1  df2 test_comp test_value p_comp reported_p  computed_p
#> 1         t  NA 97.7         =       2.90      =      0.005 0.004609391
#> 2         t  NA 97.2         =      -1.96      =      0.152 0.052859364
#>                          raw error decision_error one_tailed_in_txt apa_factor
#> 1   t(97.7) = 2.9, p = 0.005 FALSE          FALSE             FALSE          1
#> 2 t(97.2) = -1.96, p = 0.152  TRUE          FALSE             FALSE          1
#>                                                                                                                                                                                                                      text
#> 1                         On average researchers in the experimental (app) condition made fewer mistakes (M = 9.12) than researchers in the control (checklist) condition (M = 10.9), t(97.7) = 2.9, p = 0.005, d = 0.59.
#> 2 On average researchers in the experimental condition found the app marginally significantly more useful (M = 5.06) than researchers in the control condition found the checklist (M = 4.5), t(97.2) = -1.96, p = 0.152.
#>   section                  header div p  s              id
#> 1  method Method and Participants   2 1 11 to_err_is_human
#> 2 results                 Results   3 1  1 to_err_is_human
```
