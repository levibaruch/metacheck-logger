# Search for biblio info

Search for biblio info

## Usage

``` r
bibsearch(title, source = NA, authors = NA, strict = TRUE)
```

## Arguments

- title:

  The title of the work

- source:

  The source (journal or book)

- authors:

  The authors

- strict:

  Whether to return NULL or the best match if there isn't a single match

## Value

A data frame with citation info

## Examples

``` r
if (FALSE) { # \dontrun{
  bibsearch("Sample Size Justification", "Collabra Psychology")
} # }
```
