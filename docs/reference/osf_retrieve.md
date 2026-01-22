# Retrieve info from the OSF by ID

Retrieve info from the OSF by ID

## Usage

``` r
osf_retrieve(osf_url, id_col = 1, recursive = FALSE, find_project = FALSE)
```

## Arguments

- osf_url:

  an OSF ID or URL, or a table containing them

- id_col:

  the index or name of the column that contains OSF IDs or URLs, if id
  is a table

- recursive:

  whether to retrieve all children

- find_project:

  DEPRECATED always TRUE now - find the top-level project associated
  with a file (adds 1+ API calls)

## Value

a data frame of information

## Examples

``` r
# \donttest{
  # get info on one OSF node
  osf_retrieve("pngda")
#> Starting OSF retrieval for 1 URL...
#> * Retrieving info from pngda...
#> ...OSF retrieval complete!
#>   osf_url osf_id            name                 description osf_type public
#> 1   pngda  pngda Papercheck Test This is my test description    nodes   TRUE
#>   category registration preprint parent project
#> 1  project        FALSE    FALSE   <NA>   pngda

  # also get child nodes and files, and parent project
  osf_retrieve("https://osf.io/6nt4v", TRUE, TRUE)
#> Starting OSF retrieval for 1 URL...
#> * Retrieving info from 6nt4v...
#> ...Main retrieval complete
#> Starting retrieval of children...
#> * Retrieving children for 6nt4v...
#> * Retrieving files for 6nt4v...
#> ...OSF retrieval complete!
#>                osf_url osf_id               name        description osf_type
#> 1 https://osf.io/6nt4v  6nt4v     Processed Data The processed data    nodes
#> 2                 <NA>  75qgk processed-data.csv               <NA>    files
#>   public category registration preprint parent project kind filetype size
#> 1   TRUE     data        FALSE    FALSE  ckjef   pngda <NA>     <NA>   NA
#> 2     NA     <NA>           NA       NA  6nt4v   pngda file     data  185
#>   downloads                   download_url
#> 1        NA                           <NA>
#> 2       229 https://osf.io/download/75qgk/
# }
```
