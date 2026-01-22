# Set or get metacheck verbosity

Set or get metacheck verbosity

## Usage

``` r
verbose(verbose = NULL)
```

## Arguments

- verbose:

  if logical, sets whether to show verbose output messages and progress
  bars

## Value

the current option value (logical)

## Examples

``` r
verbose()
#> <request>
#> Options:
#> * debugfunction: function (type, msg) 
#> {
#>     switch(type + 1, text = if (info) prefix_message("*  ", msg), headerIn = prefix_message("<- ", msg), headerOut = prefix_message("-> ", msg), dataIn = if (data_in) prefix_message("<<  ", msg, TRUE), dataOut = if (data_out) prefix_message(">> ", msg, TRUE), sslDataIn = if (ssl && data_in) prefix_message("*< ", msg, TRUE), sslDataOut = if (ssl && data_out) prefix_message("*> ", msg, TRUE))
#> }
#> * verbose: TRUE
```
