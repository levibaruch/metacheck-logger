# Validate Papers

A quick function to help diagnose problems with imported papers. It
checks if there is a title, doi, abstract, and a bibliography

## Usage

``` r
paper_validate(paper)
```

## Arguments

- paper:

  a paper object or a list of paper objects

## Value

a list or data frame of checks

## Examples

``` r
paper_validate(psychsci[[1]])
#> $id
#> [1] "0956797613520608"
#> 
#> $valid
#> [1] TRUE
#> 
#> $doi
#> [1] ""
#> 
#> $title
#> [1] ""
#> 
#> $abstract
#> [1] ""
#> 
#> $bib
#> [1] 41
#> 
paper_validate(psychsci)
#> # A tibble: 250 × 6
#>    id               valid doi   title abstract    bib
#>  * <chr>            <lgl> <chr> <chr> <chr>     <int>
#>  1 0956797613520608 TRUE  ""    ""    ""           41
#>  2 0956797614522816 TRUE  ""    ""    ""           26
#>  3 0956797614527830 TRUE  ""    ""    ""           38
#>  4 0956797614557697 TRUE  ""    ""    ""           41
#>  5 0956797614560771 FALSE ""    ""    "missing"     5
#>  6 0956797614566469 FALSE ""    ""    "missing"    14
#>  7 0956797615569001 TRUE  ""    ""    ""           47
#>  8 0956797615569889 TRUE  ""    ""    ""           52
#>  9 0956797615583071 TRUE  ""    ""    ""           43
#> 10 0956797615588467 TRUE  ""    ""    ""           37
#> # ℹ 240 more rows
```
