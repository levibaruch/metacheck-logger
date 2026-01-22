# Concatenate tables

Concatenate tables across a list of paper objects

## Usage

``` r
concat_tables(papers, name_path)
```

## Arguments

- papers:

  a list of paper objects

- name_path:

  a vector of names that get you to the table

## Value

a merged table

## Examples

``` r
biblio <- concat_tables(psychsci[1:10], "bib")
xrefs <- concat_tables(psychsci[1:10], "xrefs")
```
