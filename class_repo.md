Homework 1
================
Bihui Sun
2018-09-15

Problem 1
=========

``` r
x = runif(n=10,min=0,max=5)
x
```

    ##  [1] 2.832908 2.863364 4.097464 1.143281 3.452052 4.695622 1.135822
    ##  [8] 1.479998 2.439280 4.347568

``` r
sum(x > 2)
```

    ## [1] 7

-   Therefore, there are 7 elements greater than 2.

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
y=tibble(
  vec_char=1:10,
  vec_factor=factor(c("Male","Male","Female","Male","Female","Male","Female","Female","Female","Male"))
)
y
```

    ## # A tibble: 10 x 2
    ##    vec_char vec_factor
    ##       <int> <fct>     
    ##  1        1 Male      
    ##  2        2 Male      
    ##  3        3 Female    
    ##  4        4 Male      
    ##  5        5 Female    
    ##  6        6 Male      
    ##  7        7 Female    
    ##  8        8 Female    
    ##  9        9 Female    
    ## 10       10 Male
