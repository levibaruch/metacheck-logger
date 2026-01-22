# Get paper from XML or text file

This should work with XML files in TEI (grobid), JATS APA-DTD, NLM-DTD
and cermine formats, plus basic parsing of plain text files.

## Usage

``` r
read(filename)

read_grobid(filename)

read_cermine(filename)

read_text(filename)
```

## Arguments

- filename:

  the path to the file, a vector of file paths, or the path to a
  directory

## Value

A paper object with class scivrs_paper, or a list of paper objects

## Examples

``` r
# paper <- read(filename)
```
