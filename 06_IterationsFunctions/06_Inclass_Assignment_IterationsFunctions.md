### Question 1.

**Regarding reproducibility, what is the main point of writing your own
functions and iterations?**

**Answer:** While copy pasting the code, it is very cumbersome sometimes
and also might cause the copy paste error in the code making it
difficult to make it reporducible. The function is created to reiterate
the same operation over different input values. Creating iteration of
the function help us to loop over the same function over and over
without causing manual error.

### Question 2.

**In your own words, describe how to write a function and a for loop in
R and how they work. Give me specifics like syntax, where to write code,
and how the results are returned.**

**Answer:** I start by naming a function and use function() command to
mention the input data that would be required by the function we are
trying to build (input goes in the small bracket). Then, a curly bracket
is started to define and describe how a function work in an equation or
formula and where the input data are plugged in the equation. Then, the
return command prints what you want to print from the equation or
formula you have used in your function. return command provides the
desired output for the function. Example: Sachi \<- function(a,b) {
result \<- a=1*2 b=2*3 return(result) } (Sachi is the name of function
here. (a,b) is the input data required for the function and is plugged
in into the formula. After the curly bracket opens, it is the space to
write the formula. return command provide what we want to output from
the formula as the result of the function used.)

We start with for() and we mention the iteration inside the paranthesis
mentioning what that range of iteration is for the function we are
using. We can use seq_along() to provide where we want to have iteration
on by assigning it to the variable (i). We can also use rep() to provide
the range of iteration for the dataset using baseR. Then we can start
curly bracket paranthesis to provide the code that we need to run
through each iteration. We can use print command to print() to print the
data as output for each iteration.

### Question 3.

**Read in the Cities.csv file from Canvas using a relative file path.**

``` r
cities <- read.csv("06_IterationsFunctions/Cities.csv")
```

### Question 4.

**Write a function to calculate the distance between two pairs of
coordinates based on the Haversine formula (see below). The input into
the function should be lat1, lon1, lat2, and lon2. The function should
return the object distance_km. All the code below needs to go into the
function.**

``` r
#creating a function
Haversine <- function(lat1, lon1, lat2, lon2){ #these are required input when the function is made and ready to state
  rad.lat1 <- lat1 * pi/180 #plugged in value of input data
rad.lon1 <- lon1 * pi/180
rad.lat2 <- lat2 * pi/180
rad.lon2 <- lon2 * pi/180
delta_lat <- rad.lat2 - rad.lat1
delta_lon <- rad.lon2 - rad.lon1
a <- sin(delta_lat / 2)^2 + cos(rad.lat1) * cos(rad.lat2) * sin(delta_lon / 2)^2
c <- 2 * asin(sqrt(a))
earth_radius <- 6378137
distance_km <- (earth_radius * c)/1000
return(distance_km) #return the value we want as output for functions
}
 #just to check if the function worked!
Haversine(1,2,3,4)
```

    ## [1] 314.7552

### Question 5.

**Using your function, compute the distance between Auburn, AL and New
York City**

1.  Subset/filter the Cities.csv data to include only the latitude and
    longitude values you need and input as input to your function.

``` r
#Load library
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

``` r
#Use the function into the dataframe that is subsetted for city, lattitude and longitude
cities1 <- cities %>% 
select(city, lat, long) %>% 
subset(cities$city == c("New York", "Auburn")) %>%
 summarise(distance_km = Haversine(lat[city=="New York"], long[city =="New York"], lat[city =="Auburn"], long[city == "Auburn"]))

#Alternatively modify the function itself without subsetting data and use it in the dataframe
Haversine1 <- function(input){
  rad.lat1 <- input$lat[input$city == "New York"] * pi/180
rad.lon1 <- input$long[input$city == "New York"] * pi/180
rad.lat2 <- input$lat[input$city == "Auburn"]* pi/180
rad.lon2 <- input$long[input$city == "Auburn"]* pi/180
delta_lat <- rad.lat2 - rad.lat1
delta_lon <- rad.lon2 - rad.lon1
a <- sin(delta_lat / 2)^2 + cos(rad.lat1) * cos(rad.lat2) * sin(delta_lon / 2)^2
c <- 2 * asin(sqrt(a))
earth_radius <- 6378137
distance_km <- (earth_radius * c)/1000
return(distance_km)
}

Haversine1(cities)
```

    ## [1] 1367.854

2.  The output of your function should be 1367.854 km

### Question 6.

**Now, use your function within a for loop to calculate the distance
between all other cities in the data. The output of the first 9
iterations is shown below.**

``` r
#output for the distance between Auburn and other cities
for (i in seq_along(cities$city)) {
  a <- Haversine(lat1 = cities$lat[i], lon1 = cities$long[i],  lat2 = cities$lat[cities$city == "Auburn"], lon2 = cities$long[cities$city == "Auburn"])
  print(a)
  }
```

    ## [1] 1367.854
    ## [1] 3051.838
    ## [1] 1045.521
    ## [1] 916.4138
    ## [1] 993.0298
    ## [1] 1056.022
    ## [1] 1239.973
    ## [1] 162.5121
    ## [1] 1036.99
    ## [1] 1665.699
    ## [1] 2476.255
    ## [1] 1108.229
    ## [1] 3507.959
    ## [1] 3388.366
    ## [1] 2951.382
    ## [1] 1530.2
    ## [1] 591.1181
    ## [1] 1363.207
    ## [1] 1909.79
    ## [1] 1380.138
    ## [1] 2961.12
    ## [1] 2752.814
    ## [1] 1092.259
    ## [1] 796.7541
    ## [1] 3479.538
    ## [1] 1290.549
    ## [1] 3301.992
    ## [1] 1191.666
    ## [1] 608.2035
    ## [1] 2504.631
    ## [1] 3337.278
    ## [1] 800.1452
    ## [1] 1001.088
    ## [1] 732.5906
    ## [1] 1371.163
    ## [1] 1091.897
    ## [1] 1043.273
    ## [1] 851.3423
    ## [1] 1382.372
    ## [1] 0

Bonus point if you can have the output of each iteration append a new
row to a dataframe, generating a new column of data. In other words, the
loop should create a dataframe with three columns called city1, city2,
and distance_km, as shown below. The first six rows of the dataframe are
shown below.

``` r
#to comparison between Auburn with other cities by creating 3 columns        
compare<-NULL
for (i in seq_along(cities$city)) {
  a <- Haversine(lat1 = cities$lat[i], lon1 = cities$long[i],  lat2 = cities$lat[cities$city == "Auburn"], lon2 = cities$long[cities$city == "Auburn"])
  compare <- rbind(
        compare,
        data.frame(
          city1 = cities$city[i],
          city2 = cities$city[cities$city == "Auburn"],
          distance_km = a))
}
```

### Question 7.

Commit and push a gfm .md file to GitHub inside a directory called
Coding Challenge 6. Provide me a link to your github written as a
clickable link in your .pdf or .docx

The folder is **06_IterationsFunctions** and file is
**06_InClass_Assignment_IterationsFunctions.md**

[Link to my
Github](06_IterationsFunctions/06_InClass_Assignment_IterationsFunctions.md)
