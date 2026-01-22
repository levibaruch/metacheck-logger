# Search text

Search the text of a paper or list of paper objects. Also works on the
table results of a `search_text()` call.

## Usage

``` r
search_text(
  paper,
  pattern = ".*",
  section = NULL,
  return = c("sentence", "paragraph", "div", "section", "match", "id"),
  ignore.case = TRUE,
  fixed = FALSE,
  perl = FALSE,
  exclude = FALSE,
  search_header = FALSE
)
```

## Arguments

- paper:

  a paper object or a list of paper objects

- pattern:

  the regex pattern to search for, if a vector with length \> 1, the
  patterns will be searched separately and combined

- section:

  the section(s) to search in

- return:

  the kind of text to return, the full sentence, paragraph, div, or
  section that the text is in, or just the (regex) match, or all body
  text for a paper (id)

- ignore.case:

  whether to ignore case when text searching

- fixed:

  logical. If TRUE, pattern is a string to be matched as is. Overrides
  all conflicting arguments.

- perl:

  logical. Should Perl-compatible regexps be used?

- exclude:

  should matches be included or excluded

- search_header:

  also search the header

## Value

a data frame of matches

## Examples

``` r
filename <- demoxml()
paper <- read(filename)

search_text(paper, "p\\s*(=|<)\\s*[0-9\\.]+", return = "match")
#> # A tibble: 2 × 7
#>   text       section header                    div     p     s id             
#>   <chr>      <chr>   <chr>                   <dbl> <dbl> <int> <chr>          
#> 1 p = 0.005  method  Method and Participants     2     1    11 to_err_is_human
#> 2 p = 0.152. results Results                     3     1     1 to_err_is_human
```
