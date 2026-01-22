# Get paper information in a table

Get paper information in a table

## Usage

``` r
info_table(
  paper,
  info = c("filename", "title", "keywords", "doi"),
  path = c("relative", "absolute")
)
```

## Arguments

- paper:

  a paper object or a list of paper objects

- info:

  a vector of columns to return

- path:

  whether to return absolute or relative path for the filename

## Value

a data frame with each paper id and info columns

## Examples

``` r
info_table(psychsci[1:10])
#> # A tibble: 10 × 5
#>    id               filename               title                  keywords doi  
#>    <chr>            <chr>                  <chr>                  <chr>    <chr>
#>  1 0956797613520608 ./0956797613520608.xml Continuous Theta-Burs… "mirror… 10.1…
#>  2 0956797614522816 ./0956797614522816.xml Beyond Gist: Strategi… ""       10.1…
#>  3 0956797614527830 ./0956797614527830.xml Serotonin and Social … "social… 10.1…
#>  4 0956797614557697 ./0956797614557697.xml Action-Specific Disru… "percep… 10.1…
#>  5 0956797614560771 ./0956797614560771.xml Emotional Vocalizatio… ""       10.1…
#>  6 0956797614566469 ./0956797614566469.xml Conspiracist Ideation… ""       10.1…
#>  7 0956797615569001 ./0956797615569001.xml Childhood Self-Contro… "person… 10.1…
#>  8 0956797615569889 ./0956797615569889.xml Failing to Forget: In… "memory… 10.1…
#>  9 0956797615583071 ./0956797615583071.xml Computer Game Play Re… "intrus… 10.1…
#> 10 0956797615588467 ./0956797615588467.xml Neural Affective Mech… "affect… 10.1…
```
