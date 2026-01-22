# Text features

Text features

## Usage

``` r
text_features(
  text,
  words,
  word_count = TRUE,
  has_number = TRUE,
  has_symbol = c(has_equals = "="),
  stem_language = "porter",
  values = c("presence", "count")
)
```

## Arguments

- text:

  a vector of the text strings to extract features from

- words:

  a vector of words to find

- word_count:

  whether to include word count

- has_number:

  whether to code the presence of numbers

- has_symbol:

  a named vector of symbols to detect

- stem_language:

  the language to use for stemming words, from
  SnowballC::getStemLanguages(), set to FALSE for no stemming

- values:

  whether to return the count of words (0+) in a string or the presence
  (0/1)

## Value

a data frame of features for each text
