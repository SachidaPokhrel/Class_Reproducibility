This is an example of R code.

This is how we can include figures

``` r
library(ggplot2)
data("mtcars")
ggplot(mtcars, aes(x=wt, y=mpg))+
  geom_point()
```

![](04_RMarkdown_files/figure-gfm/Include%20figures-1.png)<!-- -->

## R markdown formatting options

\#First level header

\##Second level header \####sub header for second level header \###Third
level header

*this text is italics* \#single asteric for italics beginning and at the
end of line **This text is bold** \#double asteric to make it bold

-one item -another item -sub item
