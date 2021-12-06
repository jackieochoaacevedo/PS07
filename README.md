PS07-Animation in R
================

# Using Gapminder for animation

This article describes how to create animation in R using the gganimate
R package.

According to the article,*gganimate: How to Create Plots with Beautiful
Animation in R*, “Gganimate is an extension of the ggplot2 package for
creating animated ggplots. It provides a range of new functionality that
can be added to the plot object in order to customize how it should
change with time.”

These are the following key features of gganimate stated from the
article:

1.Transitions: you want your data to change

2.Views: you want your viewpoint to change

3.Shadows: you want the animation to have memory

## The Packages needed

``` r
library(ggplot2)
library(gganimate)
theme_set(theme_bw())
library(gapminder)
```

## Static Plot

Note: the following code is also taken from the article

``` r
p <- ggplot(
  gapminder, 
  aes(x = gdpPercap, y=lifeExp, size = pop, colour = country)
  ) +
  geom_point(show.legend = FALSE, alpha = 0.7) +
  scale_color_viridis_d() +
  scale_size(range = c(2, 12)) +
  scale_x_log10() +
  labs(x = "GDP per capita", y = "Life expectancy")
p
```

![](README_files/figure-gfm/pressure-1.png)<!-- -->

## The Basics

1.  `transition_time()`. The transition length between the states will
    be set to correspond to the actual time difference between them.

2.  Label variables: `frame_time`. Gives the time that the current frame
    corresponds to

## Applying the Basics for transitions through years

``` r
p + facet_wrap(~continent) +
  transition_time(year) +
  labs(title = "Year: {frame_time}")
```

![](README_files/figure-gfm/unnamed-chunk-1-1.gif)<!-- -->

## Reference

This is the citation [1]

[1] Alboukadel, Transition_reveal, Draga, Tiago, W, C., Danhrogers,
Thaung, K., Sylvan, Kassambara, Kebede, M., Ankit, G, P., Saldaña, S.,
Mark, Lockwood, R. N., Petchulia, Z., Samuel, D. D. K., Artjuch, D.,
Mehmet, & Anthony. (2019, December 25). Gganimate: How to create plots
with beautiful animation in R. Datanovia. Retrieved December 3, 2021,
from
<https://www.datanovia.com/en/blog/gganimate-how-to-create-plots-with->
beautiful-animation-in-r/.
