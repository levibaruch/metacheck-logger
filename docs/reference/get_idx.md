# Get index from id

Get the index from id for an item in the hypotheses, analyses, or data
sections of a study object

## Usage

``` r
get_idx(study, id = NULL, section = "hypotheses")
```

## Arguments

- study:

  A study list object with class scivrs_study

- id:

  The id for the section (index or character) if NULL, assigns to the
  last item in the list

- section:

  The section to search, c("hypotheses", "analyses", "data")

## Value

A numeric index
