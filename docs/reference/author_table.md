# Get author information in a table

Get author information in a table

## Usage

``` r
author_table(paper)
```

## Arguments

- paper:

  a paper object or a list of paper objects

## Value

a data frame of author information

## Examples

``` r
paper <- psychsci[1:2]
author_table(paper)
#> # A tibble: 10 × 6
#>    name.surname name.given email                         affiliation id        n
#>    <chr>        <chr>      <chr>                         <chr>       <chr> <int>
#>  1 Michael      John       "johnmichaelaarhus@gmail.com" Center for… 0956…     1
#>  2 Sandberg     Kristian   ""                            Cognitive … 0956…     2
#>  3 Skewes       Joshua     ""                            Interactin… 0956…     3
#>  4 Wolf         Thomas     ""                            Program in… 0956…     4
#>  5 Blicher      Jakob      ""                            Cognitive … 0956…     5
#>  6 Overgaard    Morten     ""                            Center of … 0956…     6
#>  7 Frith        Chris D    ""                            Department… 0956…     7
#>  8 Malcolm      George L   "glmalcolm@gwu.edu"           The George… 0956…     1
#>  9 Nuthmann     Antje      ""                            University… 0956…     2
#> 10 Schyns       Philippe G ""                            Department… 0956…     3
```
