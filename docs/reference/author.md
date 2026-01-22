# Author in CRediT Format

Author in CRediT Format

## Usage

``` r
author(surname, given = "", orcid = NULL, roles = c(), ...)
```

## Arguments

- surname:

  a character string with the author's last name(s)

- given:

  a character string with the author's given name(s)

- orcid:

  the author's unique ORCiD (see https://orcid.org/)

- roles:

  a vector of roles from the CRediT taxonomy (see
  https://casrai.org/credit/); use credit_roles() to view the full list

- ...:

  further info to add to author object

## Value

a list with class scivrs_author
