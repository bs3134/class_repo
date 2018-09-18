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
    ##  1 0.185 FALSE 1995/03/18 Male  
    ##  2 1.94  FALSE 1996/03/18 Male  
    ##  3 1.63  FALSE 1997/03/18 Female
    ##  4 3.65  TRUE  1998/03/18 Male  
    ##  5 1.46  FALSE 1999/03/18 Female
    ##  6 0.324 FALSE 2000/03/18 Male  
    ##  7 1.92  FALSE 2001/03/18 Female
    ##  8 2.73  TRUE  2002/03/18 Female
    ##  9 0.673 FALSE 2003/03/18 Female
    ## 10 2.58  TRUE  2004/03/18 Male

``` r
guess_1=as.numeric(data_hw$logic)
guess_1
```

    ##  [1] 0 0 0 1 0 0 0 1 0 1

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

-   The mean of unif is 1.7087849
-   The mean of logic is 0.3
-   The mean of char is NA
-   The mean of fact is NA
