# Create a Report

Run specified modules on a paper and generate a report in quarto (qmd),
html, or pdf format.

## Usage

``` r
report(
  paper,
  modules = c("prereg_check", "funding_check", "coi_check", "power", "code_check",
    "stat_check", "stat_p_exact", "stat_p_nonsig", "stat_effect_size", "marginal",
    "ref_doi_check", "ref_replication", "ref_retraction", "ref_pubpeer"),
  output_file = paste0(paper$name, "_report.", output_format),
  output_format = c("html", "qmd"),
  args = list()
)
```

## Arguments

- paper:

  a paper object

- modules:

  a vector of modules to run (names for built-in modules or paths for
  custom modules)

- output_file:

  the name of the output file

- output_format:

  the format to create the report in

- args:

  a list of arguments to pass to modules (see Details)

## Value

the file path the report is saved to

## Details

Pass arguments to modules in a named list of lists, using the same names
as the `modules` argument. You only need to specify modules with
arguments.

    args <- list(power = list(seed = 8675309))

## Examples

``` r
# \donttest{
filename <- demoxml()
paper <- read(filename)
report(paper)
#> Starting OSF retrieval for 3 URLs...
#> * Retrieving info from 48ncu...
#> * Retrieving info from 5tbm9...
#> * Retrieving info from 629bx...
#> ...Main retrieval complete
#> Starting retrieval of children...
#> * Retrieving children for 629bx...
#> * Retrieving files for 629bx...
#> ...OSF retrieval complete!
#> * Retrieving files from https://researchbox.org/4377...
#> Downloading to: /var/folders/t6/7x6md_5s2j5bfb324s784yzw0000gn/T//Rtmp4i41MP/rbx_1769117692/archive.zip
#> Unzipping into: /var/folders/t6/7x6md_5s2j5bfb324s784yzw0000gn/T//Rtmp4i41MP/rbx_1769117692/unzipped
# }
```
