### Question 1.

Read Data

``` r
#load data
Metadata <- read.csv("05_DataWrangling/Metadata.csv", na.strings = "na")
DiversityData <- read.csv("05_DataWrangling/DiversityData.csv", na.strings = "na")
#load library
library(tidyverse)
```

    ## ── Attaching core tidyverse packages ──────────────────────── tidyverse 2.0.0 ──
    ## ✔ dplyr     1.1.4     ✔ readr     2.1.5
    ## ✔ forcats   1.0.0     ✔ stringr   1.5.1
    ## ✔ ggplot2   3.5.1     ✔ tibble    3.2.1
    ## ✔ lubridate 1.9.4     ✔ tidyr     1.3.1
    ## ✔ purrr     1.0.4     
    ## ── Conflicts ────────────────────────────────────────── tidyverse_conflicts() ──
    ## ✖ dplyr::filter() masks stats::filter()
    ## ✖ dplyr::lag()    masks stats::lag()
    ## ℹ Use the conflicted package (<http://conflicted.r-lib.org/>) to force all conflicts to become errors

### Question 2.

Combine two dataset with one common column “Code”

``` r
alpha <- left_join(Metadata, DiversityData, by = "Code")
```

### Question 3.

Calculate Pielou’s evenness index: Shannon/log(richness)

``` r
alpha_even = mutate(alpha, even = shannon/log(richness))
```

### Question 4.

Use mutate function to make a new dataset with summarise function and
piping in tidyverse

``` r
alpha_average <- alpha_even %>% 
  group_by(Crop, Time_Point) %>% 
  summarise(mean.even = mean(even),
            n = n(),
            sd.dev=sd(even)) %>% 
  mutate(std.err = sd.dev/sqrt(n))
```

    ## `summarise()` has grouped output by 'Crop'. You can override using the
    ## `.groups` argument.

``` r
alpha_average
```

    ## # A tibble: 12 × 6
    ## # Groups:   Crop [3]
    ##    Crop    Time_Point mean.even     n  sd.dev std.err
    ##    <chr>        <int>     <dbl> <int>   <dbl>   <dbl>
    ##  1 Cotton           0     0.820     6 0.00556 0.00227
    ##  2 Cotton           6     0.805     6 0.00920 0.00376
    ##  3 Cotton          12     0.767     6 0.0157  0.00640
    ##  4 Cotton          18     0.755     5 0.0169  0.00755
    ##  5 Soil             0     0.814     6 0.00765 0.00312
    ##  6 Soil             6     0.810     6 0.00587 0.00240
    ##  7 Soil            12     0.798     6 0.00782 0.00319
    ##  8 Soil            18     0.800     5 0.0104  0.00465
    ##  9 Soybean          0     0.822     6 0.00270 0.00110
    ## 10 Soybean          6     0.764     6 0.0400  0.0163 
    ## 11 Soybean         12     0.687     6 0.0643  0.0263 
    ## 12 Soybean         18     0.716     6 0.0153  0.00626

### Question 5.

Calculate the difference between the soybean column, the soil column,
and the difference between the cotton column and the soil column

``` r
alpha_average2 <- alpha_average %>% 
  select(Time_Point, Crop, mean.even) %>% 
  pivot_wider(names_from = Crop, values_from = mean.even) %>% 
  mutate(diff.cotton.even = Soil - Cotton) %>% 
  mutate(diff.soybean.even = Soil - Soybean)
```

### Question 6.

Integrating the data into plot after converting the data into the longer
version for the differences

``` r
#load library
library(ggplot2)
alpha_average2 %>% 
  select(Time_Point, diff.cotton.even, diff.soybean.even) %>% 
  pivot_longer(c(diff.cotton.even, diff.soybean.even), names_to = "diff") %>% 
  ggplot(aes(x=Time_Point, y=value, color = diff))+
  geom_line(stat = "identity")+
  xlab("Time (hrs)")+
  ylab("Difference from soil in Pielou's evenness")+
  theme_classic()
```

![](05_InClass_Assignment_DataWrangling_files/figure-gfm/Making%20datset%20longer%20format%20and%20integrating%20into%20the%20plot-1.png)<!-- -->

### Question 7.

#### Push to github

##### The folder is **05_DataWrangling** and the assignment has the file name **InClass_Assignment_DataWrangling.md**

[Link to my
GitHub](https://github.com/SachidaPokhrel/Class_Reproducibility/tree/main)
