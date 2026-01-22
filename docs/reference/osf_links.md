# Find OSF Links in Papers

OSF links can be tricky to find in PDFs, since they can insert spaces in
odd places, and view-only links that contain a ? are often interpreted
as being split across sentences. This function is our best attempt at
catching and fixing them all.

## Usage

``` r
osf_links(paper)
```

## Arguments

- paper:

  a paper object or paperlist object

## Value

a table with the OSF url in the first (text) column

## Examples

``` r
osf_links(psychsci)
#> # A tibble: 656 × 7
#>    text                                   section header   div     p     s id   
#>    <chr>                                  <chr>   <chr>  <dbl> <dbl> <int> <chr>
#>  1 osf.io/e2aks                           annex   "Open…    15     1     1 0956…
#>  2 osf.io/tvyxz/                          annex   "Open…    15     1     4 0956…
#>  3 osf.io/tvyxz/                          availa… ""        20     1     6 0956…
#>  4 osf.io/t9j8e/? view_only=f171281f212f… annex   "Open…    21     1     1 0956…
#>  5 osf .io/ideta                          availa… ""        15     1     1 0956…
#>  6 osf.io/tvyxz/                          availa… ""        15     1     4 0956…
#>  7 osf.io/eky4s                           annex   "Open…    12     1     1 0956…
#>  8 osf.io/tvyxz/                          annex   "Open…    12     1     4 0956…
#>  9 osf.io/tvyxz/                          discus… "Open…     9     1     4 0956…
#> 10 osf.io/xgwhk                           availa… "Open…    20     1     1 0956…
#> # ℹ 646 more rows
```
