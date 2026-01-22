# Get DOI from Reference

Get DOI from Reference

## Usage

``` r
get_doi(reference, min_score = 50)
```

## Arguments

- reference:

  the full text reference of the paper to get info for

- min_score:

  minimal score that is taken to be a reliable match (default 50)

## Value

doi

## Examples

``` r
ref <- paste(
  "Lakens, D., Mesquida, C., Rasti, S., & Ditroilo, M. (2024).",
  "The benefits of preregistration and Registered Reports.",
  "Evidence-Based Toxicology, 2(1)."
)
# \donttest{
  doi <- get_doi(ref)
# }
```
