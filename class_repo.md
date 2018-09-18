Homework 1
================
Bihui Sun
2018-09-15

Problem 1
=========

``` r
library(tidyverse)
```

    ## -- Attaching packages -------------------------------------------------------------------------------- tidyverse 1.2.1 --

    ## v ggplot2 3.0.0     v purrr   0.2.5
    ## v tibble  1.4.2     v dplyr   0.7.6
    ## v tidyr   0.8.1     v stringr 1.3.1
    ## v readr   1.1.1     v forcats 0.3.0

    ## -- Conflicts ----------------------------------------------------------------------------------- tidyverse_conflicts() --
    ## x dplyr::filter() masks stats::filter()
    ## x dplyr::lag()    masks stats::lag()

``` r
data_hw=tibble(
  unif = runif(n=10,min=0,max=5),
  logic= unif>2,
  char = c("1995/03/18","1996/03/18","1997/03/18","1998/03/18","1999/03/18","2000/03/18","2001/03/18","2002/03/18","2003/03/18","2004/03/18"),
  fact = factor(c("Male","Male","Female","Male","Female","Male","Female","Female","Female","Male"))
)
data_hw
```

    ## # A tibble: 10 x 4
    ##     unif logic char       fact  
    ##    <dbl> <lgl> <chr>      <fct> 
    ##  1 2.73  TRUE  1995/03/18 Male  
    ##  2 0.980 FALSE 1996/03/18 Male  
    ##  3 3.54  TRUE  1997/03/18 Female
    ##  4 0.240 FALSE 1998/03/18 Male  
    ##  5 4.59  TRUE  1999/03/18 Female
    ##  6 4.27  TRUE  2000/03/18 Male  
    ##  7 3.16  TRUE  2001/03/18 Female
    ##  8 3.31  TRUE  2002/03/18 Female
    ##  9 2.07  TRUE  2003/03/18 Female
    ## 10 1.48  FALSE 2004/03/18 Male

``` r
guess_1=as.numeric(data_hw$logic)
guess_1
```

    ##  [1] 1 0 1 0 1 1 1 1 1 0

``` r
guess_2=as.numeric(data_hw$char)
```

    ## Warning: NAs introduced by coercion

``` r
guess_2
```

    ##  [1] NA NA NA NA NA NA NA NA NA NA

``` r
guess_3=as.numeric(data_hw$fact)
guess_3
```

    ##  [1] 2 2 1 2 1 2 1 1 1 2

``` r
guess_4=as.character(data_hw$fact)
guess_4
```

    ##  [1] "Male"   "Male"   "Female" "Male"   "Female" "Male"   "Female"
    ##  [8] "Female" "Female" "Male"

-   The mean of unif is 2.638552
-   The mean of logic is 0.7
-   The mean of char is NA
-   The mean of fact is NA
