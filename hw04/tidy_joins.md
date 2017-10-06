Homework 4 - Tidy data and joins
================
Hayden Scheiber -
06 October, 2017

[Return to Main Page](https://github.com/HScheiber/STAT545-hw-Scheiber-Hayden/blob/master/README.md)

[Return to Homework 4 Landing Page](README.md)

------------------------------------------------------------------------

-   [General data reshaping and relationship to aggregation](#General-data-reshaping-and-relationship-to-aggregation)

-   [2 - Look at the spread of GDP per capita within the continents](#2---look-at-the-spread-of-gdp-per-capita-within-the-continents)

-   [3 - Compute a trimmed mean of life expectancy for different years](#3---compute-a-trimmed-mean-of-life-expectancy-for-different-years)

-   [4 - How is life expectancy changing over time on different continents?](#4---how-is-life-expectancy-changing-over-time-on-different-continents?)

-   [5 - Report the relative abundance of countries with low life expectancy over time by continent](#5---report-the-relative-abundance-of-countries-with-low-life-expectancy-over-time-by-continent)

------------------------------------------------------------------------

Welcome! This is the data wrangling and reshaping skills development, as part of STAT 545 assignment 4.

First we need to load the `gapminder` dataset and the `tidyverse` package, as well as `knitr` for nicer table outputs. When making my plots I realized that I needed to re-shaped a data-frame using a function from `reshape2`, so I load that library as well.

``` r
suppressPackageStartupMessages(library(gapminder))
suppressPackageStartupMessages(library(tidyverse))
suppressPackageStartupMessages(library(knitr))
suppressPackageStartupMessages(library(reshape2))
```

General data reshaping and relationship to aggregation
------------------------------------------------------