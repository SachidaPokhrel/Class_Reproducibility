## Functions

``` r
#make a vector 
z <- c(1:200) 

#calculate mean 
mean(z)
```

    ## [1] 100.5

``` r
#calculate standard deviation
sd(z)
```

    ## [1] 57.87918

``` r
#make a new logical dataset of the vector z
zlog <- z>30

#make dataframe for z and zlog
zdf <- data.frame(z, zlog)

#define column names for the columns of the dataframe, zdf
colnames(zdf) <- c("zvec", "zlogic")

#generating a squared zvec in a new column
zdf$zsquared <- ((zdf$zvec)^2)

#subsetting the zsquared for greater than 10 and less than 100
zdf$zsquared[zdf$zsquared>10 & zdf$zsquared<100]
```

    ## [1] 16 25 36 49 64 81

``` r
#using subset function
subset(zdf$zsquared, zdf$zsquared>10 & zdf$zsquared < 100)
```

    ## [1] 16 25 36 49 64 81

``` r
#taking 26th row
zdf [26,]
```

    ##    zvec zlogic zsquared
    ## 26   26  FALSE      676

``` r
#taking zsquared value for 180th column
zdf [180,3]
```

    ## [1] 32400

## Reading CSV file

``` r
datum1 <-read.csv("01_Functions/TipsR.csv")
datum2 <-read.csv("01_Functions/TipsR.csv", na.strings = ".")
```
