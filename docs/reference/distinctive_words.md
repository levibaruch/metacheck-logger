# Get Distinctive Words

Get Distinctive Words

## Usage

``` r
distinctive_words(
  text,
  classification,
  n = Inf,
  stop_words = c(),
  numbers = c("any", "specific", "remove"),
  stem_language = "porter",
  min_total = length(text)/10
)
```

## Arguments

- text:

  a vector of text to assess

- classification:

  a vector of the classification

- n:

  the number of top distinctive words to get

- stop_words:

  a vector or data frame of words to exclude

- numbers:

  what to do with numeric values: "any", "specific", "remove"

- stem_language:

  the language to use for stemming words, from
  SnowballC::getStemLanguages(), set to FALSE for no stemming

- min_total:

  the minimum total number of incidences to include a word, defaults to
  10% of the number of text strings

## Value

a data frame of the words
