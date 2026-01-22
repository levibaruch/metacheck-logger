# Process a paper using the Pytacheck API

Process a paper using the Pytacheck API

## Usage

``` r
pytacheck(
  file_path,
  api_url = "https://api.metacheck.app/get-paper-metadata/",
  api_key = Sys.getenv("PYTACHECK_API")
)
```

## Arguments

- file_path:

  Path to the PDF file

- api_url:

  Base URL of the API

- api_key:

  Key to access pytacheck

## Value

A list of parsed information
