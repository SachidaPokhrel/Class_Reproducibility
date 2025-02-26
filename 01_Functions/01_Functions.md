``` r
# 1 hashtag is for comment

####This is a section (4 hashtags) ####

#R is case sensitive

#Basic operators in R
#Concept of different Data types
#Load Packages in R
#Load data in R from .csv and .txt files
```

## Types of variables

``` r
#R is a big calculator
2+2
```

    ## [1] 4

``` r
2-2
```

    ## [1] 0

``` r
2/2
```

    ## [1] 1

``` r
2*2
```

    ## [1] 4

``` r
#Objects
#Numeric variables
x <- 2 #X is equals to 2, assigning value to object
y = 3 # = works same as <-

x+y
```

    ## [1] 5

``` r
x-y
```

    ## [1] -1

``` r
#Character variables
name <- "Sachi"
seven <- "7"

#x + seven #This won't work since R considers the variable to be character if in quotation though that is a number
```

## Functions in R

Functions Function is something that does something to objects. Function
opens with paranthesis

``` r
class(x) #Example
```

    ## [1] "numeric"

``` r
class(seven)
```

    ## [1] "character"

``` r
#Concatenate function
vec <- c(1, 2, 3, 4, 5, 6, 7)
vec1 <- c(1:7)
vec2 <- 1:7
vec3 <- c("Sachi", "Arpan", "BP")
vec4 <- c(TRUE, FALSE, TRUE)


vec[4] #the big bracket gives the 4th value of the vector initially created
```

    ## [1] 4

``` r
vec3[1]
```

    ## [1] "Sachi"

``` r
vec + 2
```

    ## [1] 3 4 5 6 7 8 9

``` r
##Basic function in R
vec
```

    ## [1] 1 2 3 4 5 6 7

``` r
mean(vec)
```

    ## [1] 4

``` r
sd(vec)
```

    ## [1] 2.160247

``` r
sum(vec)
```

    ## [1] 28

``` r
median(vec)
```

    ## [1] 4

``` r
min(vec)
```

    ## [1] 1

``` r
max(vec)
```

    ## [1] 7

``` r
summary(vec) #summary stats
```

    ##    Min. 1st Qu.  Median    Mean 3rd Qu.    Max. 
    ##     1.0     2.5     4.0     4.0     5.5     7.0

``` r
abs(vec) #absolute value
```

    ## [1] 1 2 3 4 5 6 7

``` r
sqrt(vec) #squareroot
```

    ## [1] 1.000000 1.414214 1.732051 2.000000 2.236068 2.449490 2.645751

``` r
sqrt(sum(vec)) ##closure for each paranthesis is necessary for running a function
```

    ## [1] 5.291503

``` r
log(vec) #natural log
```

    ## [1] 0.0000000 0.6931472 1.0986123 1.3862944 1.6094379 1.7917595 1.9459101

``` r
log10(vec)
```

    ## [1] 0.0000000 0.3010300 0.4771213 0.6020600 0.6989700 0.7781513 0.8450980

``` r
exp(vec)
```

    ## [1]    2.718282    7.389056   20.085537   54.598150  148.413159  403.428793
    ## [7] 1096.633158

## Logical operators in R

``` r
###Exercise Number 3###
## Logical operators
# > greater than
# < less than
# | or
# & and
# = equals (used to assign value from left to right)
# == exactly equal to (used to showing equality btween values)
# >= greater than or equal to
# != not equals to

1>2
```

    ## [1] FALSE

``` r
1<2
```

    ## [1] TRUE

``` r
1<=2
```

    ## [1] TRUE

``` r
1==1 #asking if 1 equal to 1 or not
```

    ## [1] TRUE

``` r
one=1 #1=1 won't work since it cannot assign same numeric value to the same numeric object

t <- 1:10

#values of t "such that" (big bracket) t is greater than 8 or less than 5
t[(t>8)|(t<5)]
```

    ## [1]  1  2  3  4  9 10

``` r
#value of t such that is greater than 8 and less than 10
t[(t>8)&(t<10)]
```

    ## [1] 9

``` r
#ask R if a number exist in a vector
32 %in% t #use of %in%
```

    ## [1] FALSE

## Data types

``` r
# scalar object
x
```

    ## [1] 2

``` r
# vector object
t
```

    ##  [1]  1  2  3  4  5  6  7  8  9 10

``` r
##matrices
#numeric matrix
mat1 <- matrix(data = c(1,2,3), nrow = 3, ncol = 3)
mat1
```

    ##      [,1] [,2] [,3]
    ## [1,]    1    1    1
    ## [2,]    2    2    2
    ## [3,]    3    3    3

``` r
#character matrix
mat2 <- matrix(data = c("Sachi", "Arpan", "BP"), nrow = 3, ncol = 3)
mat2
```

    ##      [,1]    [,2]    [,3]   
    ## [1,] "Sachi" "Sachi" "Sachi"
    ## [2,] "Arpan" "Arpan" "Arpan"
    ## [3,] "BP"    "BP"    "BP"

``` r
#giving single dimension
mat1[1]
```

    ## [1] 1

``` r
mat1[2]
```

    ## [1] 2

``` r
mat1[3]
```

    ## [1] 3

``` r
mat1[4]
```

    ## [1] 1

``` r
mat1[9]
```

    ## [1] 3

``` r
#giving 2 dimension
mat1[1,3] #1st row, 3rd column
```

    ## [1] 1

``` r
mat1[1,] #print 1st row and all columns
```

    ## [1] 1 1 1

``` r
mat1[,3] #prints 3rd column, all rows
```

    ## [1] 1 2 3

## Dataframes

Dataframes are basically like matrices but with multiple data classes or
data types (i.e., logical AND numeric)

``` r
df <- data.frame(mat1[,1], mat2[,1])
df
```

    ##   mat1...1. mat2...1.
    ## 1         1     Sachi
    ## 2         2     Arpan
    ## 3         3        BP

``` r
colnames(df) <- c("values", "name")
df[1] #dataframe 1 gives entire 1st column here
```

    ##   values
    ## 1      1
    ## 2      2
    ## 3      3

``` r
df[1,2] #first row second column
```

    ## [1] "Sachi"

``` r
df[,"values"]
```

    ## [1] 1 2 3

``` r
df$values #accessing columns
```

    ## [1] 1 2 3

``` r
df$values[1]
```

    ## [1] 1

``` r
df$name[3]
```

    ## [1] "BP"

## Subsetting or indexing

Reducing large data frame to smaller without editing the original data
for running certain analysis

``` r
#subsetting the element of the column values such that name equal to Sachi (restricting the columns such that it only has the rows of values that has Sachi in the name)
df$values[df$name == "Sachi"]
```

    ## [1] 1

``` r
df$values[df$name %in% c("Sachi", "BP")]
```

    ## [1] 1 3

``` r
df$values[df$name != "Arpan"]
```

    ## [1] 1 3

``` r
df$values[!df$name %in% c("Sachi", "BP")] # ! before the data frame gives not equal to vaues that will be mentioned later
```

    ## [1] 2

``` r
#Subset function
subset(df, name == "Sachi")
```

    ##   values  name
    ## 1      1 Sachi

``` r
#making a new column in a dataframe
df$log_value <- log(df$value)
df
```

    ##   values  name log_value
    ## 1      1 Sachi 0.0000000
    ## 2      2 Arpan 0.6931472
    ## 3      3    BP 1.0986123

\###Installing packages

``` r
#tidyverse
#purrr
#lme4

#install.packages("tidyverse")
#if (!require("BiocManager", quietly = TRUE))
 #   install.packages("BiocManager")

#BiocManager::install("phyloseq")

library(tidyverse) #loads the function into R
```

    ## ── Attaching core tidyverse packages ──────────────────────── tidyverse 2.0.0 ──
    ## ✔ dplyr     1.1.4     ✔ readr     2.1.5
    ## ✔ forcats   1.0.0     ✔ stringr   1.5.1
    ## ✔ ggplot2   3.5.1     ✔ tibble    3.2.1
    ## ✔ lubridate 1.9.4     ✔ tidyr     1.3.1
    ## ✔ purrr     1.0.2     
    ## ── Conflicts ────────────────────────────────────────── tidyverse_conflicts() ──
    ## ✖ dplyr::filter() masks stats::filter()
    ## ✖ dplyr::lag()    masks stats::lag()
    ## ℹ Use the conflicted package (<http://conflicted.r-lib.org/>) to force all conflicts to become errors

## Reading data into R

``` r
# csv or txt file
csv <- read.csv("C:/Users/pokhr/OneDrive - Auburn University/SplitPlateTrials/2024-09-16_SplitPlate_B52.csv", na.strings = "na")

#csv2 <- read.csv(file.choose(), na.strings ="na") #another way to read file
```
