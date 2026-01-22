# Batch Processing

``` r
library(metacheck)
library(dplyr) # for data wrangling
library(readr) # reading and writing CSV files
```

In this vignette, we will process 250 open access papers from
Psychological Science.

## Convert PDFs

Read in all of the PDF files from a directory called “pdf”, process them
with a local version of grobid, and save the XML files in a directory
called “xml”.

``` r
pdf2grobid(filename = "pdf", 
           save_path = "xml", 
           grobid_url = "http://localhost:8070")
```

Then read in the XML files to metacheck and save in an object called
`papers`.

``` r
papers <- read("xml")
```

These steps can take some time if you are processing a lot of papers,
and only needs to happen once, so it is often useful to save the
`papers` object as an Rds file, comment out the code above, and load
`papers` from this object on future runs of your script.

``` r
# load from RDS for efficiency
# saveRDS(papers, "psysci_oa.Rds")
papers <- readRDS("psysci_oa.Rds")
```

## Paper Objects

Now `papers` is a list of metacheck paper objects, each of which
contains structured information about the paper.

``` r
paper <- papers[[10]]
```

### ID

The `id` is taken from the name of the xml file.

``` r
paper$id
```

    #> [1] "0956797615588467"

### Authors

The `authors` list contains a list of information for each author. For
now, CRediT roles are not detected, but this may be added in the future.

``` r
paper$authors |> str()
```

    #> List of 2
    #>  $ :List of 5
    #>   ..$ orcid      : NULL
    #>   ..$ name       :List of 2
    #>   .. ..$ surname: chr "Genevsky"
    #>   .. ..$ given  : chr "Alexander"
    #>   ..$ roles      : NULL
    #>   ..$ email      : chr "genevsky@stanford.edu"
    #>   ..$ affiliation:List of 1
    #>   .. ..$ :List of 1
    #>   .. .. ..$ department: chr "Department of Psychology"
    #>   ..- attr(*, "class")= chr [1:2] "scivrs_author" "list"
    #>  $ :List of 5
    #>   ..$ orcid      : NULL
    #>   ..$ name       :List of 2
    #>   .. ..$ surname: chr "Knutson"
    #>   .. ..$ given  : chr "Brian"
    #>   ..$ roles      : NULL
    #>   ..$ email      : chr ""
    #>   ..$ affiliation:List of 2
    #>   .. ..$ :List of 1
    #>   .. .. ..$ department: chr "Department of Psychology"
    #>   .. ..$ :List of 2
    #>   .. .. ..$ department : chr "Stanford Neurosciences Institute"
    #>   .. .. ..$ institution: chr "Stanford University"
    #>   ..- attr(*, "class")= chr [1:2] "scivrs_author" "list"
    #>  - attr(*, "class")= chr [1:2] "scivrs_authors" "list"

You can get the authors as a table for a paper object or list of papers.

``` r
author_table(psychsci) |> 
  dplyr::filter(grepl("Glasgow", affiliation))
```

    #> # A tibble: 17 × 7
    #>    name.surname name.given  email                  affiliation id        n orcid
    #>    <chr>        <chr>       <chr>                  <chr>       <chr> <int> <chr>
    #>  1 Schyns       Philippe G  ""                     Department… 0956…     3 NA   
    #>  2 Lages        Martin      "martin.lages@glasgow… School of … 0956…     1 NA   
    #>  3 Boyle        Stephanie C ""                     Institute … 0956…     2 NA   
    #>  4 Jones        Benedict C  "ben.jones@glasgow.ac… Institute … 0956…     1 NA   
    #>  5 Fisher       Claire I    ""                     Institute … 0956…     3 NA   
    #>  6 Wang         Hongyi      ""                     Institute … 0956…     4 NA   
    #>  7 Kandrik      Michal      ""                     Institute … 0956…     5 NA   
    #>  8 Han          Chengyang   ""                     Institute … 0956…     6 NA   
    #>  9 Fasolt       Vanessa     ""                     Institute … 0956…     7 NA   
    #> 10 Morrison     Danielle    ""                     Institute … 0956…     8 NA   
    #> 11 Lee          Anthony J   ""                     Institute … 0956…     9 NA   
    #> 12 Holzleitner  Iris J      ""                     Institute … 0956…    10 NA   
    #> 13 O'shea       Kieran J    ""                     Institute … 0956…    11 NA   
    #> 14 Debruine     Lisa M      ""                     Institute … 0956…    14 NA   
    #> 15 Jones        Benedict C  ""                     Institute … 0956…     2 NA   
    #> 16 Debruine     Lisa M      ""                     Institute … 0956…     3 NA   
    #> 17 Fasolt       Vanessa     ""                     Institute … 0956…     5 NA

### Info

The `info` item lists the filename, title, description (abstract),
keywords, doi, and submission info. Grobid sometimes makes mistakes with
the DOI, so be cautious about using this.

``` r
paper$info
```

    #> $title
    #> [1] "Neural Affective Mechanisms Predict Market-Level Microlending"
    #> 
    #> $description
    #> [1] "Humans sometimes share with others whom they may never meet or know, in violation of the dictates of pure selfinterest. Research has not established which neuropsychological mechanisms support lending decisions, nor whether their influence extends to markets involving significant financial incentives. In two studies, we found that neural affective mechanisms influence the success of requests for microloans. In a large Internet database of microloan requests (N = 13,500), we found that positive affective features of photographs promoted the success of those requests. We then established that neural activity (i.e., in the nucleus accumbens) and self-reported positive arousal in a neuroimaging sample (N = 28) predicted the success of loan requests on the Internet, above and beyond the effects of the neuroimaging sample's own choices (i.e., to lend or not). These findings suggest that elicitation of positive arousal can promote the success of loan requests, both in the laboratory and on the Internet. They also highlight affective neuroscience's potential to probe neuropsychological mechanisms that drive microlending, enhance the effectiveness of loan requests, and forecast market-level behavior."
    #> 
    #> $keywords
    #> [1] "affect"       "accumbens"    "microlending" "preference"   "fMRI"        
    #> [6] "prosocial"    "human"       
    #> 
    #> $doi
    #> [1] "10.1177/0956797615588467"
    #> 
    #> $submission
    #> [1] "Received 2/2/15; Revision accepted 5/4/15"
    #> 
    #> $received
    #> [1] "2015-02-02"
    #> 
    #> $accepted
    #> [1] "2015-05-04"
    #> 
    #> $filename
    #> [1] "./0956797615588467.xml"

You can get this as a table for a batch of papers using
[`info_table()`](https://scienceverse.github.io/metacheck/reference/info_table.md).

``` r
info_table(papers, info = c("doi", "title")) |> 
  head()
```

    #> # A tibble: 6 × 3
    #>   id               doi                      title                               
    #>   <chr>            <chr>                    <chr>                               
    #> 1 0956797613520608 10.1177/0956797613520608 Continuous Theta-Burst Stimulation …
    #> 2 0956797614522816 10.1177/0956797614522816 Beyond Gist: Strategic and Incremen…
    #> 3 0956797614527830 10.1177/0956797614527830 Serotonin and Social Norms: Tryptop…
    #> 4 0956797614557697 10.1177/0956797614557697 Action-Specific Disruption of Perce…
    #> 5 0956797614560771 10.1177/0956797614560771 Emotional Vocalizations Are Recogni…
    #> 6 0956797614566469 10.1177/0956797614566469 Conspiracist Ideation as a Predicto…

### Bibliography

The `bib` contains the items in the reference list, including an id to
link them to cross references (xref_id), the DOI if available (doi), the
full reference text (ref), and the reference parsed by title, author,
year, etc.

``` r
bib <- paper$bib

dplyr::filter(bib, xref_id == "b5")
```

    #>   xref_id
    #> 1      b5
    #>                                                                                                                                                  ref
    #> 1 10.1016/j.jcps.2011.05.001, A neural predictor of cultural popularity, G, S, Berns, S, E, Moore, Journal of Consumer Psychology, 2012, 22, 154-160
    #>                          doi bibtype                                     title
    #> 1 10.1016/j.jcps.2011.05.001 Article A neural predictor of cultural popularity
    #>                          journal year              authors               id
    #> 1 Journal of Consumer Psychology 2012 G S Berns, S E Moore 0956797615588467

### Cross References

The `xrefs` contains each reference, including an id to link them to the
bibliography (xref_id), the sentence that they are cited in (text), and
location data.

``` r
xrefs <- paper$xrefs

dplyr::filter(xrefs, xref_id == "b5")
```

    #> # A tibble: 3 × 9
    #>   xref_id type  contents               text      id    section   div     p     s
    #>   <chr>   <chr> <chr>                  <chr>     <chr> <chr>   <dbl> <dbl> <int>
    #> 1 b5      bibr  (Berns & Moore, 2012)  Stimulus… 0956… method      4     5     7
    #> 2 b5      bibr  Berns and Moore (2012) Followin… 0956… results     7     4     2
    #> 3 b5      bibr  (Berns & Moore, 2012)  For inst… 0956… discus…     8     2     2

### Full Text

The `full_text` item is a table containing each sentence from the main
text (`text`). The heading text (`header`) is used to automatically
determine if the `section` is abstract, intro, method, results, or
discussion. Each section has a unique sequential `div` number, and each
paragraph (`p`) within the section and eeach sentence (`s`) within each
paragraph are also sequentially numbered (e.g., div = 1, p = 2, s = 3 is
the third sentence of the second paragraph of the first section after
the abstract).

``` r
paper$full_text |> names()
```

    #> [1] "text"    "section" "header"  "div"     "p"       "s"       "id"

## Text Search

The
[`search_text()`](https://scienceverse.github.io/metacheck/reference/search_text.md)
function helps you search the text of a paper or list of papers.

The default arguments give you a data frame containing a row for every
sentence in every paper in the set. The data frame has the same column
structure as the `full_text` table above, so that you can easily chain
text searches.

``` r
all_sentences <- search_text(papers)
```

You can customise
[`search_text()`](https://scienceverse.github.io/metacheck/reference/search_text.md)
to return paragraphs or sections instead of sentences. The `section`
column contains the automatically classified section types from the
options “abstract”, “intro”, “methods”, “results”, or “discussion” (this
can be inaccurate if grobid doesn’t detect headers or the header text
doesn’t obviously fall in one of these categories).

``` r
method_paragraphs <- search_text(papers, section = "method", return = "paragraph")
```

A random paragraph from a method section.

    #> [1] "Method"

### Pattern

You can just code every sentence or paragraph in a set of papers, but
this is usually not very efficient, so we can use a search pattern to
filter the text.

``` r
search <- search_text(papers, pattern = "Scotland")
```

Here we have 9 results. We’ll just show the paper id and text columns of
the returned table, but the table also provides the section type,
header, and section, paragraph, and sentence numbers (div, p, and s).

### Chaining

You can chain together searches to iteratively narrow down results.

``` r
search <- papers |>
  search_text("DeBruine") |>
  search_text("2006")
```

### Regex

You can also use regular expressions to refine your search. The pattern
below returns every sentence that contains either “Scotland” or
“Scottish”.

``` r
search <- search_text(papers, pattern = "(Scotland|Scottish)")
```

### Match

You can return just the matching text for a regular expression by
setting the results to “match”. This pattern searches for text like “p
\< .25” or p\<0.01”.

``` r
match <- search_text(papers, 
                     pattern = "p\\s*>\\s*0?\\.[0-9]+\\b", 
                     return = "match")
```

You can expand this to the whole sentence, paragraph, or +/- some number
of sentences around the match using
[`expand_text()`](https://scienceverse.github.io/metacheck/reference/expand_text.md).

``` r
expand <- expand_text(results_table = match, 
                      paper = papers,
                      expand_to = "sentence",
                      plus = 0,
                      minus = 0)

expand$expanded[1]
```

    #> [1] "No main effects or interactions with time were found (p > .29), which indicates that the action-specific effects of TMS on confidence are not specific to its delivery before or after a perceptual decision."
