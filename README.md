PS07-Animation in R
================

## Gapminder

This article describes how to create animation in R using the gganimate
R package.

According to the article,*gganimate: How to Create Plots with Beautiful
Animation in R*, “Gganimate is an extension of the ggplot2 package for
creating animated ggplots. It provides a range of new functionality that
can be added to the plot object in order to customize how it should
change with time.”

These are the following key features of gganinmate stated from the article:

1.Transitions: you want your data to change 

2.Views: you want your viewpoint to change 

3.Shadows: you want the animation to have memory

## The code for animation


``` r
library(ggplot2)
library(gganimate)
theme_set(theme_bw())
library(gapminder)
head(gapminder)
```

    ## # A tibble: 6 × 6
    ##   country     continent  year lifeExp      pop gdpPercap
    ##   <fct>       <fct>     <int>   <dbl>    <int>     <dbl>
    ## 1 Afghanistan Asia       1952    28.8  8425333      779.
    ## 2 Afghanistan Asia       1957    30.3  9240934      821.
    ## 3 Afghanistan Asia       1962    32.0 10267083      853.
    ## 4 Afghanistan Asia       1967    34.0 11537966      836.
    ## 5 Afghanistan Asia       1972    36.1 13079460      740.
    ## 6 Afghanistan Asia       1977    38.4 14880372      786.

Code is taken from here: [1] ## Including Plots

You can also embed plots, for example: Note: the following code is also
taken from the article
![](README_files/figure-gfm/pressure-2.png)<!-- -->![](README_files/figure-gfm/pressure-1.gif)<!-- -->

Note that the `echo = FALSE` parameter was added to the code chunk to
prevent printing of the R code that generated the plot.
##Reference
[1] Alboukadel, Transition_reveal, Draga, Tiago, W, C., Danhrogers,
Thaung, K., Sylvan, Kassambara, Kebede, M., Ankit, G, P., Saldaña, S.,
Mark, Lockwood, R. N., Petchulia, Z., Samuel, D. D. K., Artjuch, D.,
Mehmet, & Anthony. (2019, December 25). Gganimate: How to create plots
with beautiful animation in R. Datanovia. Retrieved December 3, 2021,
from
<https://www.datanovia.com/en/blog/gganimate-how-to-create-plots-with->
beautiful-animation-in-r/.
