# Find GitHub Links in Papers

GitHub links can be in PDFs in several ways.

## Usage

``` r
github_links(paper)
```

## Arguments

- paper:

  a paper object or paperlist object

## Value

a table with the GitHub url in the first (text) column

## Examples

``` r
github_links(psychsci)
#> # A tibble: 9 × 7
#>   text                                    section header   div     p     s id   
#>   <chr>                                   <chr>   <chr>  <dbl> <dbl> <int> <chr>
#> 1 https://github.com/addrummond/ibex      method  "Meth…     2     3     3 0956…
#> 2 https://github.com/jmobrien/SpecCurve   annex   "Open…    22     1     3 0956…
#> 3 https://github.com/silveycat/vocab-syn… method  "Proc…     6     9    13 0956…
#> 4 https://github.com/silveycat/vocab-syn… availa… ""        15     1     1 0956…
#> 5 https://github.com/Spaak/context-congr… funding "Fund…    15     1     5 0956…
#> 6 https://github.com/robloughnan/ABCD_In… intro   "Open…     3     1     2 0956…
#> 7 https://github.com/giacomobignardi/emp… annex   "Open…    17     1     3 0956…
#> 8 https://github.com/kobor-lab/Public-Sc… intro   "Open…     3     1     2 0956…
#> 9 https://github.com/kobor-lab/Public-Sc… method  "Meas…     6     3     3 0956…
```
