# Find AsPredicted Links in Papers

Find AsPredicted Links in Papers

## Usage

``` r
aspredicted_links(paper)
```

## Arguments

- paper:

  a paper object or paperlist object

## Value

a table with the AsPredicted url in the first (text) column

## Examples

``` r
aspredicted_links(psychsci)
#> # A tibble: 74 × 7
#>    text                              section header        div     p     s id   
#>    <chr>                             <chr>   <chr>       <dbl> <dbl> <int> <chr>
#>  1 https://aspredicted.org/ve2qn.pdf intro   Short Repo…     2     4     3 0956…
#>  2 https://aspredicted.org/ve2qn.pdf method  Subjects        4     1     9 0956…
#>  3 https://aspredicted.org/ve2qn.pdf method  Electroenc…    10     4     1 0956…
#>  4 https://aspredicted.org/ve2qn.pdf results Results        11     2     3 0956…
#>  5 https://aspredicted.org/ve2qn.pdf annex   Supplement…    16     2     1 0956…
#>  6 https://aspredicted.org/mq97g.pdf results Experiment…    10     1     1 0956…
#>  7 https://aspredicted.org/mq97g.pdf funding Open Pract…    16     1     2 0956…
#>  8 https://aspredicted.org/4gf64.pdf intro   Distinguis…     2     2     5 0956…
#>  9 https://aspredicted.org/8a6ta.pdf method  Method          7     1     1 0956…
#> 10 https://aspredicted.org/vp4rg.pdf method  Method         11     1     1 0956…
#> # ℹ 64 more rows
```
