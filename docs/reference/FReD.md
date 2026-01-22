# FORRT Replication Database

FReD database containing DOIs of original studies and replications. Use
`fred_date()` to find the date it was downloaded, and `fred_update()` to
update it.

## Usage

``` r
FReD()
```

## Format

A data frame with 2222 rows and 4 columns:

- ref_original:

  reference of original study

- doi_original:

  doi of original study

- ref_replication:

  reference of replication study

- ref_replication:

  doi of replication study

## Source

<https://osf.io/9r62x/files/z5u9b>

## Value

a data frame

## Examples

``` r
FReD()
#> # A tibble: 2,222 × 4
#>    ref_original                     doi_original ref_replication doi_replication
#>    <chr>                            <chr>        <chr>           <chr>          
#>  1 DeWall, C. N., & Bushman, B. J.… 10.1016/j.j… "McCarthy, R. … 10.17605/OSF.I…
#>  2 Elliot, A. J., Niesta Kayser, D… 10.1037/a00… "Banas, K. (20… 10.17605/OSF.I…
#>  3 Jostmann, N. B., Lakens, D., & … 10.1111/j.1… "Djordjević, S… 10.17605/OSF.I…
#>  4 Cheung, B. Y., & Heine, S. J. (… 10.1177/014… "Crawford, J. … 10.17605/OSF.I…
#>  5 Critcher, C. R., & Gilovich, T.… 10.1002/bdm… "Fujishima, Y.… 10.17605/OSF.I…
#>  6 Knobe, J. (2003). Intentional a… 10.1080/095… "Hannikainen, … 10.17605/OSF.I…
#>  7 Cunningham, W. A., Van Bavel, J… 10.1111/j.1… "McRae, K., Lu… 10.17605/OSF.I…
#>  8 Nichols, S., & Knobe, J. (2007)… 10.1111/j.1… "Moerenhout, T… 10.17605/OSF.I…
#>  9 Wilkins, C. L., & Kaiser, C. R.… 10.1177/095… "Crawford, J. … 10.17605/OSF.I…
#> 10 Nichols, S. (2006). Folk intuit… 10.1163/156… "Cova, F. (201… 10.17605/OSF.I…
#> # ℹ 2,212 more rows
```
