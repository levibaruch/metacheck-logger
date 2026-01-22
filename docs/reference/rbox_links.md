# Find ResearchBox Links in Papers

Find ResearchBox Links in Papers

## Usage

``` r
rbox_links(paper)
```

## Arguments

- paper:

  a paper object or paperlist object

## Value

a table with the ResearchBox url in the first (text) column

## Examples

``` r
rbox_links(psychsci)
#> # A tibble: 3 × 7
#>   text                                    section header   div     p     s id   
#>   <chr>                                   <chr>   <chr>  <dbl> <dbl> <int> <chr>
#> 1 https://researchbox.org/801             intro   State…     3     3     1 0956…
#> 2 https://researchbox.org/801             funding Open …    18     1     1 0956…
#> 3 https://researchbox.org/1150&PEER_REVI… funding Open …    29     1     2 0956…
```
