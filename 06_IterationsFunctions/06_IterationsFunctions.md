## Functions

``` r
#str() #allows us to see structure of data
# (5*(degree_f - 32)/9) # to convert fanhrenheit to celsius
(5*(32- 32)/9)
```

    ## [1] 0

``` r
#we might have to copy and paste for many iterations that we might have to do!
```

### Creating Functions

``` r
#Make a function to provide the formula so that we can use the same function to reteorate different values. here our input is the f_temp where we put value and it returns as celsius while using the function F_to_C. We are saving the function to save it for use.
F_to_C <- function(f_temp){
 celsius <- (5*(f_temp - 32)/9)
 return(celsius)
}

#check with different values using the same function
F_to_C(32)
```

    ## [1] 0

``` r
F_to_C(-40)
```

    ## [1] -40

``` r
F_to_C(180)
```

    ## [1] 82.22222

``` r
#function to convert celsius to fahrenheit

C_to_F <- function(c_temp){
  fahrenheit <- (c_temp*(9/5)+32)
  return(fahrenheit)
}

#check with different values of Fahrenheit
C_to_F(-40)
```

    ## [1] -40

## Iterations

Iteration is important to prevent copy paste errors

``` r
#BaseR type iteration function
rep("A", 3) #repetition function to repeat A for 3 times
```

    ## [1] "A" "A" "A"

``` r
rep(c("A", "B"), 10)
```

    ##  [1] "A" "B" "A" "B" "A" "B" "A" "B" "A" "B" "A" "B" "A" "B" "A" "B" "A" "B" "A"
    ## [20] "B"

``` r
rep(c(1,2,5,3), 4, each = 5) #repeat the list four time with each repeated for 5 times
```

    ##  [1] 1 1 1 1 1 2 2 2 2 2 5 5 5 5 5 3 3 3 3 3 1 1 1 1 1 2 2 2 2 2 5 5 5 5 5 3 3 3
    ## [39] 3 3 1 1 1 1 1 2 2 2 2 2 5 5 5 5 5 3 3 3 3 3 1 1 1 1 1 2 2 2 2 2 5 5 5 5 5 3
    ## [77] 3 3 3 3

``` r
1:7 #outputs in the sequence
```

    ## [1] 1 2 3 4 5 6 7

``` r
seq(from =1, to = 7) #allows to have sequence of number
```

    ## [1] 1 2 3 4 5 6 7

``` r
seq(from =0, to = 10, by = 2) #by argument allows to select every second data with the gap
```

    ## [1]  0  2  4  6  8 10

``` r
LETTERS #character vector built in R
```

    ##  [1] "A" "B" "C" "D" "E" "F" "G" "H" "I" "J" "K" "L" "M" "N" "O" "P" "Q" "R" "S"
    ## [20] "T" "U" "V" "W" "X" "Y" "Z"

``` r
seq_along(LETTERS) #reference each character vector by nub=mber and replace by the values, its important at that point
```

    ##  [1]  1  2  3  4  5  6  7  8  9 10 11 12 13 14 15 16 17 18 19 20 21 22 23 24 25
    ## [26] 26

## The for loop

``` r
# The for loop works to finish off the iteration so that the sequence mentioned is over
for (i in 1:10){
 print(i*2)
} #i is the variable that includes (in) the given sequences for the value that will be used for each iteration and print command prints every iteration of the performed function to the console
```

    ## [1] 2
    ## [1] 4
    ## [1] 6
    ## [1] 8
    ## [1] 10
    ## [1] 12
    ## [1] 14
    ## [1] 16
    ## [1] 18
    ## [1] 20

## Integrate function into the for loop

``` r
for (i in -30:100){
  result <- F_to_C(i)
  print(result)
}# runs function F_to_C that we created earlier for each value of i mentioned in the iterative sequences, and prints the results for each function in the console
```

    ## [1] -34.44444
    ## [1] -33.88889
    ## [1] -33.33333
    ## [1] -32.77778
    ## [1] -32.22222
    ## [1] -31.66667
    ## [1] -31.11111
    ## [1] -30.55556
    ## [1] -30
    ## [1] -29.44444
    ## [1] -28.88889
    ## [1] -28.33333
    ## [1] -27.77778
    ## [1] -27.22222
    ## [1] -26.66667
    ## [1] -26.11111
    ## [1] -25.55556
    ## [1] -25
    ## [1] -24.44444
    ## [1] -23.88889
    ## [1] -23.33333
    ## [1] -22.77778
    ## [1] -22.22222
    ## [1] -21.66667
    ## [1] -21.11111
    ## [1] -20.55556
    ## [1] -20
    ## [1] -19.44444
    ## [1] -18.88889
    ## [1] -18.33333
    ## [1] -17.77778
    ## [1] -17.22222
    ## [1] -16.66667
    ## [1] -16.11111
    ## [1] -15.55556
    ## [1] -15
    ## [1] -14.44444
    ## [1] -13.88889
    ## [1] -13.33333
    ## [1] -12.77778
    ## [1] -12.22222
    ## [1] -11.66667
    ## [1] -11.11111
    ## [1] -10.55556
    ## [1] -10
    ## [1] -9.444444
    ## [1] -8.888889
    ## [1] -8.333333
    ## [1] -7.777778
    ## [1] -7.222222
    ## [1] -6.666667
    ## [1] -6.111111
    ## [1] -5.555556
    ## [1] -5
    ## [1] -4.444444
    ## [1] -3.888889
    ## [1] -3.333333
    ## [1] -2.777778
    ## [1] -2.222222
    ## [1] -1.666667
    ## [1] -1.111111
    ## [1] -0.5555556
    ## [1] 0
    ## [1] 0.5555556
    ## [1] 1.111111
    ## [1] 1.666667
    ## [1] 2.222222
    ## [1] 2.777778
    ## [1] 3.333333
    ## [1] 3.888889
    ## [1] 4.444444
    ## [1] 5
    ## [1] 5.555556
    ## [1] 6.111111
    ## [1] 6.666667
    ## [1] 7.222222
    ## [1] 7.777778
    ## [1] 8.333333
    ## [1] 8.888889
    ## [1] 9.444444
    ## [1] 10
    ## [1] 10.55556
    ## [1] 11.11111
    ## [1] 11.66667
    ## [1] 12.22222
    ## [1] 12.77778
    ## [1] 13.33333
    ## [1] 13.88889
    ## [1] 14.44444
    ## [1] 15
    ## [1] 15.55556
    ## [1] 16.11111
    ## [1] 16.66667
    ## [1] 17.22222
    ## [1] 17.77778
    ## [1] 18.33333
    ## [1] 18.88889
    ## [1] 19.44444
    ## [1] 20
    ## [1] 20.55556
    ## [1] 21.11111
    ## [1] 21.66667
    ## [1] 22.22222
    ## [1] 22.77778
    ## [1] 23.33333
    ## [1] 23.88889
    ## [1] 24.44444
    ## [1] 25
    ## [1] 25.55556
    ## [1] 26.11111
    ## [1] 26.66667
    ## [1] 27.22222
    ## [1] 27.77778
    ## [1] 28.33333
    ## [1] 28.88889
    ## [1] 29.44444
    ## [1] 30
    ## [1] 30.55556
    ## [1] 31.11111
    ## [1] 31.66667
    ## [1] 32.22222
    ## [1] 32.77778
    ## [1] 33.33333
    ## [1] 33.88889
    ## [1] 34.44444
    ## [1] 35
    ## [1] 35.55556
    ## [1] 36.11111
    ## [1] 36.66667
    ## [1] 37.22222
    ## [1] 37.77778

``` r
#output are not saved in the objevt rather just in the console and cannot be used for further use

## saving output by converting into dataframe
celsius.df <- NULL
for (i in -30:100){
  result <- data.frame(F_to_C(i), i) #column, row in the dataframe and prints as 1 row data frame for each iteration
  print(result)
} 
```

    ##   F_to_C.i.   i
    ## 1 -34.44444 -30
    ##   F_to_C.i.   i
    ## 1 -33.88889 -29
    ##   F_to_C.i.   i
    ## 1 -33.33333 -28
    ##   F_to_C.i.   i
    ## 1 -32.77778 -27
    ##   F_to_C.i.   i
    ## 1 -32.22222 -26
    ##   F_to_C.i.   i
    ## 1 -31.66667 -25
    ##   F_to_C.i.   i
    ## 1 -31.11111 -24
    ##   F_to_C.i.   i
    ## 1 -30.55556 -23
    ##   F_to_C.i.   i
    ## 1       -30 -22
    ##   F_to_C.i.   i
    ## 1 -29.44444 -21
    ##   F_to_C.i.   i
    ## 1 -28.88889 -20
    ##   F_to_C.i.   i
    ## 1 -28.33333 -19
    ##   F_to_C.i.   i
    ## 1 -27.77778 -18
    ##   F_to_C.i.   i
    ## 1 -27.22222 -17
    ##   F_to_C.i.   i
    ## 1 -26.66667 -16
    ##   F_to_C.i.   i
    ## 1 -26.11111 -15
    ##   F_to_C.i.   i
    ## 1 -25.55556 -14
    ##   F_to_C.i.   i
    ## 1       -25 -13
    ##   F_to_C.i.   i
    ## 1 -24.44444 -12
    ##   F_to_C.i.   i
    ## 1 -23.88889 -11
    ##   F_to_C.i.   i
    ## 1 -23.33333 -10
    ##   F_to_C.i.  i
    ## 1 -22.77778 -9
    ##   F_to_C.i.  i
    ## 1 -22.22222 -8
    ##   F_to_C.i.  i
    ## 1 -21.66667 -7
    ##   F_to_C.i.  i
    ## 1 -21.11111 -6
    ##   F_to_C.i.  i
    ## 1 -20.55556 -5
    ##   F_to_C.i.  i
    ## 1       -20 -4
    ##   F_to_C.i.  i
    ## 1 -19.44444 -3
    ##   F_to_C.i.  i
    ## 1 -18.88889 -2
    ##   F_to_C.i.  i
    ## 1 -18.33333 -1
    ##   F_to_C.i. i
    ## 1 -17.77778 0
    ##   F_to_C.i. i
    ## 1 -17.22222 1
    ##   F_to_C.i. i
    ## 1 -16.66667 2
    ##   F_to_C.i. i
    ## 1 -16.11111 3
    ##   F_to_C.i. i
    ## 1 -15.55556 4
    ##   F_to_C.i. i
    ## 1       -15 5
    ##   F_to_C.i. i
    ## 1 -14.44444 6
    ##   F_to_C.i. i
    ## 1 -13.88889 7
    ##   F_to_C.i. i
    ## 1 -13.33333 8
    ##   F_to_C.i. i
    ## 1 -12.77778 9
    ##   F_to_C.i.  i
    ## 1 -12.22222 10
    ##   F_to_C.i.  i
    ## 1 -11.66667 11
    ##   F_to_C.i.  i
    ## 1 -11.11111 12
    ##   F_to_C.i.  i
    ## 1 -10.55556 13
    ##   F_to_C.i.  i
    ## 1       -10 14
    ##   F_to_C.i.  i
    ## 1 -9.444444 15
    ##   F_to_C.i.  i
    ## 1 -8.888889 16
    ##   F_to_C.i.  i
    ## 1 -8.333333 17
    ##   F_to_C.i.  i
    ## 1 -7.777778 18
    ##   F_to_C.i.  i
    ## 1 -7.222222 19
    ##   F_to_C.i.  i
    ## 1 -6.666667 20
    ##   F_to_C.i.  i
    ## 1 -6.111111 21
    ##   F_to_C.i.  i
    ## 1 -5.555556 22
    ##   F_to_C.i.  i
    ## 1        -5 23
    ##   F_to_C.i.  i
    ## 1 -4.444444 24
    ##   F_to_C.i.  i
    ## 1 -3.888889 25
    ##   F_to_C.i.  i
    ## 1 -3.333333 26
    ##   F_to_C.i.  i
    ## 1 -2.777778 27
    ##   F_to_C.i.  i
    ## 1 -2.222222 28
    ##   F_to_C.i.  i
    ## 1 -1.666667 29
    ##   F_to_C.i.  i
    ## 1 -1.111111 30
    ##    F_to_C.i.  i
    ## 1 -0.5555556 31
    ##   F_to_C.i.  i
    ## 1         0 32
    ##   F_to_C.i.  i
    ## 1 0.5555556 33
    ##   F_to_C.i.  i
    ## 1  1.111111 34
    ##   F_to_C.i.  i
    ## 1  1.666667 35
    ##   F_to_C.i.  i
    ## 1  2.222222 36
    ##   F_to_C.i.  i
    ## 1  2.777778 37
    ##   F_to_C.i.  i
    ## 1  3.333333 38
    ##   F_to_C.i.  i
    ## 1  3.888889 39
    ##   F_to_C.i.  i
    ## 1  4.444444 40
    ##   F_to_C.i.  i
    ## 1         5 41
    ##   F_to_C.i.  i
    ## 1  5.555556 42
    ##   F_to_C.i.  i
    ## 1  6.111111 43
    ##   F_to_C.i.  i
    ## 1  6.666667 44
    ##   F_to_C.i.  i
    ## 1  7.222222 45
    ##   F_to_C.i.  i
    ## 1  7.777778 46
    ##   F_to_C.i.  i
    ## 1  8.333333 47
    ##   F_to_C.i.  i
    ## 1  8.888889 48
    ##   F_to_C.i.  i
    ## 1  9.444444 49
    ##   F_to_C.i.  i
    ## 1        10 50
    ##   F_to_C.i.  i
    ## 1  10.55556 51
    ##   F_to_C.i.  i
    ## 1  11.11111 52
    ##   F_to_C.i.  i
    ## 1  11.66667 53
    ##   F_to_C.i.  i
    ## 1  12.22222 54
    ##   F_to_C.i.  i
    ## 1  12.77778 55
    ##   F_to_C.i.  i
    ## 1  13.33333 56
    ##   F_to_C.i.  i
    ## 1  13.88889 57
    ##   F_to_C.i.  i
    ## 1  14.44444 58
    ##   F_to_C.i.  i
    ## 1        15 59
    ##   F_to_C.i.  i
    ## 1  15.55556 60
    ##   F_to_C.i.  i
    ## 1  16.11111 61
    ##   F_to_C.i.  i
    ## 1  16.66667 62
    ##   F_to_C.i.  i
    ## 1  17.22222 63
    ##   F_to_C.i.  i
    ## 1  17.77778 64
    ##   F_to_C.i.  i
    ## 1  18.33333 65
    ##   F_to_C.i.  i
    ## 1  18.88889 66
    ##   F_to_C.i.  i
    ## 1  19.44444 67
    ##   F_to_C.i.  i
    ## 1        20 68
    ##   F_to_C.i.  i
    ## 1  20.55556 69
    ##   F_to_C.i.  i
    ## 1  21.11111 70
    ##   F_to_C.i.  i
    ## 1  21.66667 71
    ##   F_to_C.i.  i
    ## 1  22.22222 72
    ##   F_to_C.i.  i
    ## 1  22.77778 73
    ##   F_to_C.i.  i
    ## 1  23.33333 74
    ##   F_to_C.i.  i
    ## 1  23.88889 75
    ##   F_to_C.i.  i
    ## 1  24.44444 76
    ##   F_to_C.i.  i
    ## 1        25 77
    ##   F_to_C.i.  i
    ## 1  25.55556 78
    ##   F_to_C.i.  i
    ## 1  26.11111 79
    ##   F_to_C.i.  i
    ## 1  26.66667 80
    ##   F_to_C.i.  i
    ## 1  27.22222 81
    ##   F_to_C.i.  i
    ## 1  27.77778 82
    ##   F_to_C.i.  i
    ## 1  28.33333 83
    ##   F_to_C.i.  i
    ## 1  28.88889 84
    ##   F_to_C.i.  i
    ## 1  29.44444 85
    ##   F_to_C.i.  i
    ## 1        30 86
    ##   F_to_C.i.  i
    ## 1  30.55556 87
    ##   F_to_C.i.  i
    ## 1  31.11111 88
    ##   F_to_C.i.  i
    ## 1  31.66667 89
    ##   F_to_C.i.  i
    ## 1  32.22222 90
    ##   F_to_C.i.  i
    ## 1  32.77778 91
    ##   F_to_C.i.  i
    ## 1  33.33333 92
    ##   F_to_C.i.  i
    ## 1  33.88889 93
    ##   F_to_C.i.  i
    ## 1  34.44444 94
    ##   F_to_C.i.  i
    ## 1        35 95
    ##   F_to_C.i.  i
    ## 1  35.55556 96
    ##   F_to_C.i.  i
    ## 1  36.11111 97
    ##   F_to_C.i.  i
    ## 1  36.66667 98
    ##   F_to_C.i.  i
    ## 1  37.22222 99
    ##   F_to_C.i.   i
    ## 1  37.77778 100

``` r
celsius.df <- NULL
for (i in -30:100){
  result <- data.frame(F_to_C(i), i) #column, row in the dataframe and prints as 1 row data frame for each iteration
  print(result)
  celsius.df <- rbind.data.frame(celsius.df, result) # rbind stands for row bind that binds the dataframe output from the previous iteration to the new output iteration forming a combined dataframe
} 
```

    ##   F_to_C.i.   i
    ## 1 -34.44444 -30
    ##   F_to_C.i.   i
    ## 1 -33.88889 -29
    ##   F_to_C.i.   i
    ## 1 -33.33333 -28
    ##   F_to_C.i.   i
    ## 1 -32.77778 -27
    ##   F_to_C.i.   i
    ## 1 -32.22222 -26
    ##   F_to_C.i.   i
    ## 1 -31.66667 -25
    ##   F_to_C.i.   i
    ## 1 -31.11111 -24
    ##   F_to_C.i.   i
    ## 1 -30.55556 -23
    ##   F_to_C.i.   i
    ## 1       -30 -22
    ##   F_to_C.i.   i
    ## 1 -29.44444 -21
    ##   F_to_C.i.   i
    ## 1 -28.88889 -20
    ##   F_to_C.i.   i
    ## 1 -28.33333 -19
    ##   F_to_C.i.   i
    ## 1 -27.77778 -18
    ##   F_to_C.i.   i
    ## 1 -27.22222 -17
    ##   F_to_C.i.   i
    ## 1 -26.66667 -16
    ##   F_to_C.i.   i
    ## 1 -26.11111 -15
    ##   F_to_C.i.   i
    ## 1 -25.55556 -14
    ##   F_to_C.i.   i
    ## 1       -25 -13
    ##   F_to_C.i.   i
    ## 1 -24.44444 -12
    ##   F_to_C.i.   i
    ## 1 -23.88889 -11
    ##   F_to_C.i.   i
    ## 1 -23.33333 -10
    ##   F_to_C.i.  i
    ## 1 -22.77778 -9
    ##   F_to_C.i.  i
    ## 1 -22.22222 -8
    ##   F_to_C.i.  i
    ## 1 -21.66667 -7
    ##   F_to_C.i.  i
    ## 1 -21.11111 -6
    ##   F_to_C.i.  i
    ## 1 -20.55556 -5
    ##   F_to_C.i.  i
    ## 1       -20 -4
    ##   F_to_C.i.  i
    ## 1 -19.44444 -3
    ##   F_to_C.i.  i
    ## 1 -18.88889 -2
    ##   F_to_C.i.  i
    ## 1 -18.33333 -1
    ##   F_to_C.i. i
    ## 1 -17.77778 0
    ##   F_to_C.i. i
    ## 1 -17.22222 1
    ##   F_to_C.i. i
    ## 1 -16.66667 2
    ##   F_to_C.i. i
    ## 1 -16.11111 3
    ##   F_to_C.i. i
    ## 1 -15.55556 4
    ##   F_to_C.i. i
    ## 1       -15 5
    ##   F_to_C.i. i
    ## 1 -14.44444 6
    ##   F_to_C.i. i
    ## 1 -13.88889 7
    ##   F_to_C.i. i
    ## 1 -13.33333 8
    ##   F_to_C.i. i
    ## 1 -12.77778 9
    ##   F_to_C.i.  i
    ## 1 -12.22222 10
    ##   F_to_C.i.  i
    ## 1 -11.66667 11
    ##   F_to_C.i.  i
    ## 1 -11.11111 12
    ##   F_to_C.i.  i
    ## 1 -10.55556 13
    ##   F_to_C.i.  i
    ## 1       -10 14
    ##   F_to_C.i.  i
    ## 1 -9.444444 15
    ##   F_to_C.i.  i
    ## 1 -8.888889 16
    ##   F_to_C.i.  i
    ## 1 -8.333333 17
    ##   F_to_C.i.  i
    ## 1 -7.777778 18
    ##   F_to_C.i.  i
    ## 1 -7.222222 19
    ##   F_to_C.i.  i
    ## 1 -6.666667 20
    ##   F_to_C.i.  i
    ## 1 -6.111111 21
    ##   F_to_C.i.  i
    ## 1 -5.555556 22
    ##   F_to_C.i.  i
    ## 1        -5 23
    ##   F_to_C.i.  i
    ## 1 -4.444444 24
    ##   F_to_C.i.  i
    ## 1 -3.888889 25
    ##   F_to_C.i.  i
    ## 1 -3.333333 26
    ##   F_to_C.i.  i
    ## 1 -2.777778 27
    ##   F_to_C.i.  i
    ## 1 -2.222222 28
    ##   F_to_C.i.  i
    ## 1 -1.666667 29
    ##   F_to_C.i.  i
    ## 1 -1.111111 30
    ##    F_to_C.i.  i
    ## 1 -0.5555556 31
    ##   F_to_C.i.  i
    ## 1         0 32
    ##   F_to_C.i.  i
    ## 1 0.5555556 33
    ##   F_to_C.i.  i
    ## 1  1.111111 34
    ##   F_to_C.i.  i
    ## 1  1.666667 35
    ##   F_to_C.i.  i
    ## 1  2.222222 36
    ##   F_to_C.i.  i
    ## 1  2.777778 37
    ##   F_to_C.i.  i
    ## 1  3.333333 38
    ##   F_to_C.i.  i
    ## 1  3.888889 39
    ##   F_to_C.i.  i
    ## 1  4.444444 40
    ##   F_to_C.i.  i
    ## 1         5 41
    ##   F_to_C.i.  i
    ## 1  5.555556 42
    ##   F_to_C.i.  i
    ## 1  6.111111 43
    ##   F_to_C.i.  i
    ## 1  6.666667 44
    ##   F_to_C.i.  i
    ## 1  7.222222 45
    ##   F_to_C.i.  i
    ## 1  7.777778 46
    ##   F_to_C.i.  i
    ## 1  8.333333 47
    ##   F_to_C.i.  i
    ## 1  8.888889 48
    ##   F_to_C.i.  i
    ## 1  9.444444 49
    ##   F_to_C.i.  i
    ## 1        10 50
    ##   F_to_C.i.  i
    ## 1  10.55556 51
    ##   F_to_C.i.  i
    ## 1  11.11111 52
    ##   F_to_C.i.  i
    ## 1  11.66667 53
    ##   F_to_C.i.  i
    ## 1  12.22222 54
    ##   F_to_C.i.  i
    ## 1  12.77778 55
    ##   F_to_C.i.  i
    ## 1  13.33333 56
    ##   F_to_C.i.  i
    ## 1  13.88889 57
    ##   F_to_C.i.  i
    ## 1  14.44444 58
    ##   F_to_C.i.  i
    ## 1        15 59
    ##   F_to_C.i.  i
    ## 1  15.55556 60
    ##   F_to_C.i.  i
    ## 1  16.11111 61
    ##   F_to_C.i.  i
    ## 1  16.66667 62
    ##   F_to_C.i.  i
    ## 1  17.22222 63
    ##   F_to_C.i.  i
    ## 1  17.77778 64
    ##   F_to_C.i.  i
    ## 1  18.33333 65
    ##   F_to_C.i.  i
    ## 1  18.88889 66
    ##   F_to_C.i.  i
    ## 1  19.44444 67
    ##   F_to_C.i.  i
    ## 1        20 68
    ##   F_to_C.i.  i
    ## 1  20.55556 69
    ##   F_to_C.i.  i
    ## 1  21.11111 70
    ##   F_to_C.i.  i
    ## 1  21.66667 71
    ##   F_to_C.i.  i
    ## 1  22.22222 72
    ##   F_to_C.i.  i
    ## 1  22.77778 73
    ##   F_to_C.i.  i
    ## 1  23.33333 74
    ##   F_to_C.i.  i
    ## 1  23.88889 75
    ##   F_to_C.i.  i
    ## 1  24.44444 76
    ##   F_to_C.i.  i
    ## 1        25 77
    ##   F_to_C.i.  i
    ## 1  25.55556 78
    ##   F_to_C.i.  i
    ## 1  26.11111 79
    ##   F_to_C.i.  i
    ## 1  26.66667 80
    ##   F_to_C.i.  i
    ## 1  27.22222 81
    ##   F_to_C.i.  i
    ## 1  27.77778 82
    ##   F_to_C.i.  i
    ## 1  28.33333 83
    ##   F_to_C.i.  i
    ## 1  28.88889 84
    ##   F_to_C.i.  i
    ## 1  29.44444 85
    ##   F_to_C.i.  i
    ## 1        30 86
    ##   F_to_C.i.  i
    ## 1  30.55556 87
    ##   F_to_C.i.  i
    ## 1  31.11111 88
    ##   F_to_C.i.  i
    ## 1  31.66667 89
    ##   F_to_C.i.  i
    ## 1  32.22222 90
    ##   F_to_C.i.  i
    ## 1  32.77778 91
    ##   F_to_C.i.  i
    ## 1  33.33333 92
    ##   F_to_C.i.  i
    ## 1  33.88889 93
    ##   F_to_C.i.  i
    ## 1  34.44444 94
    ##   F_to_C.i.  i
    ## 1        35 95
    ##   F_to_C.i.  i
    ## 1  35.55556 96
    ##   F_to_C.i.  i
    ## 1  36.11111 97
    ##   F_to_C.i.  i
    ## 1  36.66667 98
    ##   F_to_C.i.  i
    ## 1  37.22222 99
    ##   F_to_C.i.   i
    ## 1  37.77778 100

``` r
celsius.df #print the dataframe in console
```

    ##       F_to_C.i.   i
    ## 1   -34.4444444 -30
    ## 2   -33.8888889 -29
    ## 3   -33.3333333 -28
    ## 4   -32.7777778 -27
    ## 5   -32.2222222 -26
    ## 6   -31.6666667 -25
    ## 7   -31.1111111 -24
    ## 8   -30.5555556 -23
    ## 9   -30.0000000 -22
    ## 10  -29.4444444 -21
    ## 11  -28.8888889 -20
    ## 12  -28.3333333 -19
    ## 13  -27.7777778 -18
    ## 14  -27.2222222 -17
    ## 15  -26.6666667 -16
    ## 16  -26.1111111 -15
    ## 17  -25.5555556 -14
    ## 18  -25.0000000 -13
    ## 19  -24.4444444 -12
    ## 20  -23.8888889 -11
    ## 21  -23.3333333 -10
    ## 22  -22.7777778  -9
    ## 23  -22.2222222  -8
    ## 24  -21.6666667  -7
    ## 25  -21.1111111  -6
    ## 26  -20.5555556  -5
    ## 27  -20.0000000  -4
    ## 28  -19.4444444  -3
    ## 29  -18.8888889  -2
    ## 30  -18.3333333  -1
    ## 31  -17.7777778   0
    ## 32  -17.2222222   1
    ## 33  -16.6666667   2
    ## 34  -16.1111111   3
    ## 35  -15.5555556   4
    ## 36  -15.0000000   5
    ## 37  -14.4444444   6
    ## 38  -13.8888889   7
    ## 39  -13.3333333   8
    ## 40  -12.7777778   9
    ## 41  -12.2222222  10
    ## 42  -11.6666667  11
    ## 43  -11.1111111  12
    ## 44  -10.5555556  13
    ## 45  -10.0000000  14
    ## 46   -9.4444444  15
    ## 47   -8.8888889  16
    ## 48   -8.3333333  17
    ## 49   -7.7777778  18
    ## 50   -7.2222222  19
    ## 51   -6.6666667  20
    ## 52   -6.1111111  21
    ## 53   -5.5555556  22
    ## 54   -5.0000000  23
    ## 55   -4.4444444  24
    ## 56   -3.8888889  25
    ## 57   -3.3333333  26
    ## 58   -2.7777778  27
    ## 59   -2.2222222  28
    ## 60   -1.6666667  29
    ## 61   -1.1111111  30
    ## 62   -0.5555556  31
    ## 63    0.0000000  32
    ## 64    0.5555556  33
    ## 65    1.1111111  34
    ## 66    1.6666667  35
    ## 67    2.2222222  36
    ## 68    2.7777778  37
    ## 69    3.3333333  38
    ## 70    3.8888889  39
    ## 71    4.4444444  40
    ## 72    5.0000000  41
    ## 73    5.5555556  42
    ## 74    6.1111111  43
    ## 75    6.6666667  44
    ## 76    7.2222222  45
    ## 77    7.7777778  46
    ## 78    8.3333333  47
    ## 79    8.8888889  48
    ## 80    9.4444444  49
    ## 81   10.0000000  50
    ## 82   10.5555556  51
    ## 83   11.1111111  52
    ## 84   11.6666667  53
    ## 85   12.2222222  54
    ## 86   12.7777778  55
    ## 87   13.3333333  56
    ## 88   13.8888889  57
    ## 89   14.4444444  58
    ## 90   15.0000000  59
    ## 91   15.5555556  60
    ## 92   16.1111111  61
    ## 93   16.6666667  62
    ## 94   17.2222222  63
    ## 95   17.7777778  64
    ## 96   18.3333333  65
    ## 97   18.8888889  66
    ## 98   19.4444444  67
    ## 99   20.0000000  68
    ## 100  20.5555556  69
    ## 101  21.1111111  70
    ## 102  21.6666667  71
    ## 103  22.2222222  72
    ## 104  22.7777778  73
    ## 105  23.3333333  74
    ## 106  23.8888889  75
    ## 107  24.4444444  76
    ## 108  25.0000000  77
    ## 109  25.5555556  78
    ## 110  26.1111111  79
    ## 111  26.6666667  80
    ## 112  27.2222222  81
    ## 113  27.7777778  82
    ## 114  28.3333333  83
    ## 115  28.8888889  84
    ## 116  29.4444444  85
    ## 117  30.0000000  86
    ## 118  30.5555556  87
    ## 119  31.1111111  88
    ## 120  31.6666667  89
    ## 121  32.2222222  90
    ## 122  32.7777778  91
    ## 123  33.3333333  92
    ## 124  33.8888889  93
    ## 125  34.4444444  94
    ## 126  35.0000000  95
    ## 127  35.5555556  96
    ## 128  36.1111111  97
    ## 129  36.6666667  98
    ## 130  37.2222222  99
    ## 131  37.7777778 100

## Practical example for the loops

``` r
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

``` r
library(drc) #package for dose response curve
```

    ## Warning: package 'drc' was built under R version 4.4.3

    ## Loading required package: MASS
    ## 
    ## Attaching package: 'MASS'
    ## 
    ## The following object is masked from 'package:dplyr':
    ## 
    ##     select
    ## 
    ## 
    ## 'drc' has been loaded.
    ## 
    ## Please cite R and 'drc' if used for a publication,
    ## for references type 'citation()' and 'citation('drc')'.
    ## 
    ## 
    ## Attaching package: 'drc'
    ## 
    ## The following objects are masked from 'package:stats':
    ## 
    ##     gaussian, getInitial

``` r
#read data
EC50.data <- read.csv("06_IterationsFunctions/EC50_all.csv")
 #non-linear regression data
isolate1 <- drm(100 * EC50.data$relgrowth[EC50.data$is == "ILSO_5-41c"] ~ 
        EC50.data$conc[EC50.data$is == "ILSO_5-41c"], 
                       fct = LL.4(fixed = c(NA, NA, NA, NA), 
                                  names = c("Slope", "Lower", "Upper", "EC50")), 
                       na.action = na.omit)
    # outputs the summary of the paramters including the estimate, standard
    # error, t-value, and p-value outputs it into a data frame called
    # summary.mef.fit for 'summary of fit'
    summary.fit <- data.frame(summary(isolate1)[[3]])
    # outputs the summary of just the EC50 data including the estimate, standard
    # error, upper and lower bounds of the 95% confidence intervals around the
    # EC50
    EC50 <- ED(isolate1, respLev = c(50), type = "relative", 
        interval = "delta")[[1]]
```

    ## 
    ## Estimated effective doses
    ## 
    ##         Estimate Std. Error     Lower     Upper
    ## e:1:50 0.1070318  0.0055365 0.0957543 0.1183094

``` r
  # we need to integrate it into the for loop so that the isalte codes are swapped and the general non-linear regression is run for the next isolate
    nm <- unique(EC50.data$is)
    for (i in seq_along(nm)) {
  isolate1 <- drm(100 * EC50.data$relgrowth[EC50.data$is == nm[[i]]] ~ 
        EC50.data$conc[EC50.data$is == nm[[i]]], 
                       fct = LL.4(fixed = c(NA, NA, NA, NA), 
                                  names = c("Slope", "Lower", "Upper", "EC50")), 
                       na.action = na.omit)
  print(nm[[i]]) # print the isolate name with the summary output too
    # outputs the summary of the paramters including the estimate, standard
    # error, t-value, and p-value outputs it into a data frame called
    # summary.mef.fit for 'summary of fit'
    summary.fit <- data.frame(summary(isolate1)[[3]])
    # outputs the summary of just the EC50 data including the estimate, standard
    # error, upper and lower bounds of the 95% confidence intervals around the
    # EC50
    EC50 <- ED(isolate1, respLev = c(50), type = "relative", 
        interval = "delta")[[1]]
    EC50
    }
```

    ## [1] "ILSO_5-41c"
    ## 
    ## Estimated effective doses
    ## 
    ##         Estimate Std. Error     Lower     Upper
    ## e:1:50 0.1070318  0.0055365 0.0957543 0.1183094
    ## [1] "ILSO_5-42c"
    ## 
    ## Estimated effective doses
    ## 
    ##        Estimate Std. Error    Lower    Upper
    ## e:1:50 0.248655   0.028485 0.190633 0.306678
    ## [1] "ILSO_5-49b"
    ## 
    ## Estimated effective doses
    ## 
    ##        Estimate Std. Error    Lower    Upper
    ## e:1:50 0.167592   0.010197 0.146821 0.188362
    ## [1] "ILSO_6-1"
    ## 
    ## Estimated effective doses
    ## 
    ##         Estimate Std. Error     Lower     Upper
    ## e:1:50 0.1082677  0.0051459 0.0977858 0.1187495
    ## [1] "ILSO_6-12B"
    ## 
    ## Estimated effective doses
    ## 
    ##        Estimate Std. Error    Lower    Upper
    ## e:1:50 0.184271   0.036047 0.110846 0.257695
    ## [1] "ILSO_6-2b"
    ## 
    ## Estimated effective doses
    ## 
    ##        Estimate Std. Error    Lower    Upper
    ## e:1:50 0.227432   0.040614 0.144704 0.310160
    ## [1] "ILSO_6-33C"
    ## 
    ## Estimated effective doses
    ## 
    ##        Estimate Std. Error    Lower    Upper
    ## e:1:50 0.101863   0.003487 0.094760 0.108965
    ## [1] "ILSO_6-39C"
    ## 
    ## Estimated effective doses
    ## 
    ##         Estimate Std. Error     Lower     Upper
    ## e:1:50 0.1102721  0.0033354 0.1034780 0.1170661
    ## [1] "ILSO_6-15b"
    ## 
    ## Estimated effective doses
    ## 
    ##        Estimate Std. Error    Lower    Upper
    ## e:1:50 0.123288   0.014018 0.094735 0.151841
    ## [1] "ILSO_6-28C"
    ## 
    ## Estimated effective doses
    ## 
    ##         Estimate Std. Error     Lower     Upper
    ## e:1:50 0.0998727  0.0044787 0.0907498 0.1089956
    ## [1] "ILSO_6-34c"
    ## 
    ## Estimated effective doses
    ## 
    ##        Estimate Std. Error    Lower    Upper
    ## e:1:50  0.69465    0.39164 -0.10310  1.49240
    ## [1] "ILSO_6-35b"
    ## 
    ## Estimated effective doses
    ## 
    ##        Estimate Std. Error    Lower    Upper
    ## e:1:50 0.113975   0.012773 0.087958 0.139993
    ## [1] "ILSO_6-36b"
    ## 
    ## Estimated effective doses
    ## 
    ##        Estimate Std. Error    Lower    Upper
    ## e:1:50 0.217436   0.027934 0.160536 0.274335
    ## [1] "INSO_1-13D"
    ## 
    ## Estimated effective doses
    ## 
    ##         Estimate Std. Error     Lower     Upper
    ## e:1:50 0.1432333  0.0093132 0.1242629 0.1622036
    ## [1] "INSO_1-17C"
    ## 
    ## Estimated effective doses
    ## 
    ##        Estimate Std. Error   Lower   Upper
    ## e:1:50  0.18336    0.01293 0.15695 0.20977
    ## [1] "INSO_1-17D"
    ## 
    ## Estimated effective doses
    ## 
    ##        Estimate Std. Error    Lower    Upper
    ## e:1:50 0.186929   0.034023 0.117626 0.256232
    ## [1] "INSO_1-23-C"
    ## 
    ## Estimated effective doses
    ## 
    ##         Estimate Std. Error     Lower     Upper
    ## e:1:50 0.0299288  0.0017812 0.0263007 0.0335569
    ## [1] "INSO_1-28-C"
    ## 
    ## Estimated effective doses
    ## 
    ##        Estimate Std. Error    Lower    Upper
    ## e:1:50 0.200379   0.020104 0.159429 0.241329
    ## [1] "INSO_1-28-D"
    ## 
    ## Estimated effective doses
    ## 
    ##        Estimate Std. Error    Lower    Upper
    ## e:1:50  0.30812    0.24033 -0.18142  0.79765
    ## [1] "INSO_1-52-B"
    ## 
    ## Estimated effective doses
    ## 
    ##        Estimate Std. Error    Lower    Upper
    ## e:1:50 0.227103   0.019697 0.186983 0.267224
    ## [1] "INSO_1-53A"
    ## 
    ## Estimated effective doses
    ## 
    ##        Estimate Std. Error   Lower   Upper
    ## e:1:50  0.20009    0.01448 0.17059 0.22958
    ## [1] "INSO_2-57"
    ## 
    ## Estimated effective doses
    ## 
    ##        Estimate Std. Error    Lower    Upper
    ## e:1:50 0.223966   0.058089 0.105642 0.342290
    ## [1] "INSO_3-45"
    ## 
    ## Estimated effective doses
    ## 
    ##        Estimate Std. Error    Lower    Upper
    ## e:1:50 0.288001   0.074597 0.136052 0.439951
    ## [1] "INSO_3-49"
    ## 
    ## Estimated effective doses
    ## 
    ##        Estimate Std. Error    Lower    Upper
    ## e:1:50 0.369422   0.077015 0.212549 0.526296
    ## [1] "IASO_1-16.1h"
    ## 
    ## Estimated effective doses
    ## 
    ##        Estimate Std. Error    Lower    Upper
    ## e:1:50 0.118335   0.011733 0.094404 0.142265
    ## [1] "IASO_1-16.2r"
    ## 
    ## Estimated effective doses
    ## 
    ##        Estimate Std. Error    Lower    Upper
    ## e:1:50 0.189945   0.013146 0.163097 0.216793
    ## [1] "IASO_1-20.44rt"
    ## 
    ## Estimated effective doses
    ## 
    ##         Estimate Std. Error     Lower     Upper
    ## e:1:50 0.0483296  0.0022658 0.0437143 0.0529448
    ## [1] "IASO_10-28.24rt"
    ## 
    ## Estimated effective doses
    ## 
    ##        Estimate Std. Error    Lower    Upper
    ## e:1:50 0.190146   0.027182 0.134779 0.245514
    ## [1] "IASO_2-11.8"
    ## 
    ## Estimated effective doses
    ## 
    ##        Estimate Std. Error   Lower   Upper
    ## e:1:50  0.16580    0.01082 0.14376 0.18784
    ## [1] "IASO_6-10.15h"
    ## 
    ## Estimated effective doses
    ## 
    ##        Estimate Std. Error    Lower    Upper
    ## e:1:50 0.183297   0.017237 0.148187 0.218407
    ## [1] "IASO_6-34.31r"
    ## 
    ## Estimated effective doses
    ## 
    ##        Estimate Std. Error    Lower    Upper
    ## e:1:50 0.130147   0.010705 0.108342 0.151951
    ## [1] "IASO_9-10.4h"
    ## 
    ## Estimated effective doses
    ## 
    ##         Estimate Std. Error     Lower     Upper
    ## e:1:50 0.1915200  0.0077369 0.1757605 0.2072795
    ## [1] "IASO_9-11.1h"
    ## 
    ## Estimated effective doses
    ## 
    ##        Estimate Std. Error    Lower    Upper
    ## e:1:50 0.123034   0.006696 0.109395 0.136673
    ## [1] "IASO_9-24.27rd"
    ## 
    ## Estimated effective doses
    ## 
    ##         Estimate Std. Error     Lower     Upper
    ## e:1:50 0.1935594  0.0094277 0.1743559 0.2127629
    ## [1] "IASO_9-29.33h"
    ## 
    ## Estimated effective doses
    ## 
    ##        Estimate Std. Error    Lower    Upper
    ## e:1:50 0.198000   0.019219 0.158853 0.237148
    ## [1] "IASO_9-31.37h"
    ## 
    ## Estimated effective doses
    ## 
    ##         Estimate Std. Error     Lower     Upper
    ## e:1:50 0.1114482  0.0070542 0.0970793 0.1258172
    ## [1] "IASO_9-36.42rd"
    ## 
    ## Estimated effective doses
    ## 
    ##        Estimate Std. Error    Lower    Upper
    ## e:1:50 0.159440   0.010423 0.138209 0.180671
    ## [1] "IASO_9-4.8h"
    ## 
    ## Estimated effective doses
    ## 
    ##         Estimate Std. Error     Lower     Upper
    ## e:1:50 0.1372654  0.0070847 0.1228343 0.1516965
    ## [1] "KSSO_3-34"
    ## 
    ## Estimated effective doses
    ## 
    ##         Estimate Std. Error     Lower     Upper
    ## e:1:50  0.427766   0.230327 -0.041395  0.896927
    ## [1] "KSSO_5-21"
    ## 
    ## Estimated effective doses
    ## 
    ##         Estimate Std. Error     Lower     Upper
    ## e:1:50 0.0991738  0.0040323 0.0909603 0.1073874
    ## [1] "C-MISO2_1-19"
    ## 
    ## Estimated effective doses
    ## 
    ##        Estimate Std. Error    Lower    Upper
    ## e:1:50 0.106855   0.022010 0.062022 0.151687
    ## [1] "MISO_5-9"
    ## 
    ## Estimated effective doses
    ## 
    ##        Estimate Std. Error    Lower    Upper
    ## e:1:50 0.156127   0.021551 0.112229 0.200025
    ## [1] "MISO_8-23"
    ## 
    ## Estimated effective doses
    ## 
    ##        Estimate Std. Error    Lower    Upper
    ## e:1:50 0.308127   0.019233 0.268951 0.347304
    ## [1] "C-MNSO_6-4"
    ## 
    ## Estimated effective doses
    ## 
    ##        Estimate Std. Error    Lower    Upper
    ## e:1:50 0.117014   0.012255 0.092052 0.141977
    ## [1] "C-MNSO2_1-1"
    ## 
    ## Estimated effective doses
    ## 
    ##        Estimate Std. Error    Lower    Upper
    ## e:1:50 0.177036   0.011915 0.152767 0.201305
    ## [1] "C-MNSO2_1-19"
    ## 
    ## Estimated effective doses
    ## 
    ##        Estimate Std. Error    Lower    Upper
    ## e:1:50 0.234268   0.017095 0.199447 0.269088
    ## [1] "C-MNSO2_2-10"
    ## 
    ## Estimated effective doses
    ## 
    ##         Estimate Std. Error     Lower     Upper
    ## e:1:50 0.0172659  0.0012838 0.0146508 0.0198809
    ## [1] "MNSO_2-11"
    ## 
    ## Estimated effective doses
    ## 
    ##        Estimate Std. Error    Lower    Upper
    ## e:1:50 0.201737   0.012113 0.176998 0.226476
    ## [1] "MNSO_2-31"
    ## 
    ## Estimated effective doses
    ## 
    ##        Estimate Std. Error    Lower    Upper
    ## e:1:50 0.306968   0.078617 0.146831 0.467105
    ## [1] "MNSO_2-52"
    ## 
    ## Estimated effective doses
    ## 
    ##        Estimate Std. Error    Lower    Upper
    ## e:1:50 0.289597   0.081347 0.123464 0.455730
    ## [1] "MNSO_5-20"
    ## 
    ## Estimated effective doses
    ## 
    ##        Estimate Std. Error    Lower    Upper
    ## e:1:50 0.213191   0.024013 0.164278 0.262104
    ## [1] "NESO_1-27"
    ## 
    ## Estimated effective doses
    ## 
    ##        Estimate Std. Error    Lower    Upper
    ## e:1:50  0.42728    0.28840 -0.16016  1.01472
    ## [1] "NESO_3-20"
    ## 
    ## Estimated effective doses
    ## 
    ##         Estimate Std. Error     Lower     Upper
    ## e:1:50 0.0900834  0.0021351 0.0857344 0.0944324
    ## [1] "NESO_4-20"
    ## 
    ## Estimated effective doses
    ## 
    ##         Estimate Std. Error     Lower     Upper
    ## e:1:50 0.1573077  0.0065037 0.1440602 0.1705553
    ## [1] "NESO_4-38"
    ## 
    ## Estimated effective doses
    ## 
    ##        Estimate Std. Error   Lower   Upper
    ## e:1:50  0.16319    0.01761 0.12732 0.19906
    ## [1] "NESO_4-40"
    ## 
    ## Estimated effective doses
    ## 
    ##        Estimate Std. Error   Lower   Upper
    ## e:1:50  0.20914    0.01403 0.18056 0.23772
    ## [1] "NESO_4-42"
    ## 
    ## Estimated effective doses
    ## 
    ##        Estimate Std. Error   Lower   Upper
    ## e:1:50  0.17905    0.00849 0.16171 0.19639
    ## [1] "NESO_4-47"
    ## 
    ## Estimated effective doses
    ## 
    ##         Estimate Std. Error     Lower     Upper
    ## e:1:50 0.1587569  0.0098007 0.1387411 0.1787727
    ## [1] "NDSO_4-1"
    ## 
    ## Estimated effective doses
    ## 
    ##         Estimate Std. Error     Lower     Upper
    ## e:1:50 0.1352667  0.0074545 0.1200824 0.1504511
    ## [1] "NDSO_4-18"
    ## 
    ## Estimated effective doses
    ## 
    ##        Estimate Std. Error    Lower    Upper
    ## e:1:50 0.247784   0.036714 0.173000 0.322567
    ## [1] "NDSO_4-2"
    ## 
    ## Estimated effective doses
    ## 
    ##        Estimate Std. Error    Lower    Upper
    ## e:1:50 0.235268   0.026532 0.181223 0.289313
    ## [1] "NDSO_4-43"
    ## 
    ## Estimated effective doses
    ## 
    ##        Estimate Std. Error    Lower    Upper
    ## e:1:50 0.066926   0.010213 0.046123 0.087728
    ## [1] "NDSO_4-45"
    ## 
    ## Estimated effective doses
    ## 
    ##        Estimate Std. Error    Lower    Upper
    ## e:1:50 0.174492   0.010501 0.153102 0.195882
    ## [1] "NDSO_5-22"
    ## 
    ## Estimated effective doses
    ## 
    ##        Estimate Std. Error    Lower    Upper
    ## e:1:50 0.181951   0.028336 0.124233 0.239669
    ## [1] "NDSO_5-36"
    ## 
    ## Estimated effective doses
    ## 
    ##        Estimate Std. Error    Lower    Upper
    ## e:1:50 0.195576   0.013476 0.168125 0.223027
    ## [1] "NDSO_5-46"
    ## 
    ## Estimated effective doses
    ## 
    ##        Estimate Std. Error    Lower    Upper
    ## e:1:50 0.168410   0.010795 0.146421 0.190399
    ## [1] "NDSO_5-49"
    ## 
    ## Estimated effective doses
    ## 
    ##         Estimate Std. Error     Lower     Upper
    ## e:1:50 0.1546980  0.0093702 0.1354373 0.1739588
    ## [1] "NDSO_5-9"
    ## 
    ## Estimated effective doses
    ## 
    ##        Estimate Std. Error    Lower    Upper
    ## e:1:50 0.162666   0.011066 0.140126 0.185206
    ## [1] "C-SDSO2_5-16"
    ## 
    ## Estimated effective doses
    ## 
    ##        Estimate Std. Error    Lower    Upper
    ## e:1:50 0.147113   0.008233 0.130343 0.163883
    ## [1] "C-SDSO2_5-17"
    ## 
    ## Estimated effective doses
    ## 
    ##         Estimate Std. Error     Lower     Upper
    ## e:1:50 0.1376907  0.0077899 0.1218232 0.1535582
    ## [1] "C-SDSO2_5-29"
    ## 
    ## Estimated effective doses
    ## 
    ##        Estimate Std. Error    Lower    Upper
    ## e:1:50 0.118886   0.004502 0.109716 0.128057
    ## [1] "C-SDSO2_5-8"
    ## 
    ## Estimated effective doses
    ## 
    ##        Estimate Std. Error    Lower    Upper
    ## e:1:50 0.206342   0.016866 0.171988 0.240696
    ## [1] "C-SDSO2_5-9"
    ## 
    ## Estimated effective doses
    ## 
    ##        Estimate Std. Error    Lower    Upper
    ## e:1:50 0.175509   0.013954 0.147086 0.203932
    ## [1] "C-SDSO2_6-33"
    ## 
    ## Estimated effective doses
    ## 
    ##        Estimate Std. Error    Lower    Upper
    ## e:1:50  0.65376    0.63282 -0.63525  1.94277
    ## [1] "V-SDSO2_5-41"
    ## 
    ## Estimated effective doses
    ## 
    ##        Estimate Std. Error    Lower    Upper
    ## e:1:50 0.211026   0.012571 0.185419 0.236633

### Make the output into the data frame for the for loop

``` r
  EC50.114 <-NULL #created an empty dataframe first which will be used in the for loop to store the data or output from the loop
    nm <- unique(EC50.data$is) #extract only unique name out of the dataframe to further use it as a sequence
    for (i in seq_along(nm)) {
  isolate1 <- drm(100 * EC50.data$relgrowth[EC50.data$is == nm[[i]]] ~ 
        EC50.data$conc[EC50.data$is == nm[[i]]], 
                       fct = LL.4(fixed = c(NA, NA, NA, NA), 
                                  names = c("Slope", "Lower", "Upper", "EC50")), 
                       na.action = na.omit)
  print(nm[[i]])
    # outputs the summary of the paramters including the estimate, standard
    # error, t-value, and p-value outputs it into a data frame called
    # summary.mef.fit for 'summary of fit'
    summary.fit <- data.frame(summary(isolate1)[[3]])
    # outputs the summary of just the EC50 data including the estimate, standard
    # error, upper and lower bounds of the 95% confidence intervals around the
    # EC50
    EC50 <- ED(isolate1, respLev = c(50), type = "relative", 
        interval = "delta")[[1]]
    isolate.ec_1 <- data.frame(nm[[i]], EC50)
    EC50.114 <- rbind.data.frame(EC50.114, isolate.ec_1) #append the data into the previous datafame and overwritting it
    EC50
    }
```

    ## [1] "ILSO_5-41c"
    ## 
    ## Estimated effective doses
    ## 
    ##         Estimate Std. Error     Lower     Upper
    ## e:1:50 0.1070318  0.0055365 0.0957543 0.1183094
    ## [1] "ILSO_5-42c"
    ## 
    ## Estimated effective doses
    ## 
    ##        Estimate Std. Error    Lower    Upper
    ## e:1:50 0.248655   0.028485 0.190633 0.306678
    ## [1] "ILSO_5-49b"
    ## 
    ## Estimated effective doses
    ## 
    ##        Estimate Std. Error    Lower    Upper
    ## e:1:50 0.167592   0.010197 0.146821 0.188362
    ## [1] "ILSO_6-1"
    ## 
    ## Estimated effective doses
    ## 
    ##         Estimate Std. Error     Lower     Upper
    ## e:1:50 0.1082677  0.0051459 0.0977858 0.1187495
    ## [1] "ILSO_6-12B"
    ## 
    ## Estimated effective doses
    ## 
    ##        Estimate Std. Error    Lower    Upper
    ## e:1:50 0.184271   0.036047 0.110846 0.257695
    ## [1] "ILSO_6-2b"
    ## 
    ## Estimated effective doses
    ## 
    ##        Estimate Std. Error    Lower    Upper
    ## e:1:50 0.227432   0.040614 0.144704 0.310160
    ## [1] "ILSO_6-33C"
    ## 
    ## Estimated effective doses
    ## 
    ##        Estimate Std. Error    Lower    Upper
    ## e:1:50 0.101863   0.003487 0.094760 0.108965
    ## [1] "ILSO_6-39C"
    ## 
    ## Estimated effective doses
    ## 
    ##         Estimate Std. Error     Lower     Upper
    ## e:1:50 0.1102721  0.0033354 0.1034780 0.1170661
    ## [1] "ILSO_6-15b"
    ## 
    ## Estimated effective doses
    ## 
    ##        Estimate Std. Error    Lower    Upper
    ## e:1:50 0.123288   0.014018 0.094735 0.151841
    ## [1] "ILSO_6-28C"
    ## 
    ## Estimated effective doses
    ## 
    ##         Estimate Std. Error     Lower     Upper
    ## e:1:50 0.0998727  0.0044787 0.0907498 0.1089956
    ## [1] "ILSO_6-34c"
    ## 
    ## Estimated effective doses
    ## 
    ##        Estimate Std. Error    Lower    Upper
    ## e:1:50  0.69465    0.39164 -0.10310  1.49240
    ## [1] "ILSO_6-35b"
    ## 
    ## Estimated effective doses
    ## 
    ##        Estimate Std. Error    Lower    Upper
    ## e:1:50 0.113975   0.012773 0.087958 0.139993
    ## [1] "ILSO_6-36b"
    ## 
    ## Estimated effective doses
    ## 
    ##        Estimate Std. Error    Lower    Upper
    ## e:1:50 0.217436   0.027934 0.160536 0.274335
    ## [1] "INSO_1-13D"
    ## 
    ## Estimated effective doses
    ## 
    ##         Estimate Std. Error     Lower     Upper
    ## e:1:50 0.1432333  0.0093132 0.1242629 0.1622036
    ## [1] "INSO_1-17C"
    ## 
    ## Estimated effective doses
    ## 
    ##        Estimate Std. Error   Lower   Upper
    ## e:1:50  0.18336    0.01293 0.15695 0.20977
    ## [1] "INSO_1-17D"
    ## 
    ## Estimated effective doses
    ## 
    ##        Estimate Std. Error    Lower    Upper
    ## e:1:50 0.186929   0.034023 0.117626 0.256232
    ## [1] "INSO_1-23-C"
    ## 
    ## Estimated effective doses
    ## 
    ##         Estimate Std. Error     Lower     Upper
    ## e:1:50 0.0299288  0.0017812 0.0263007 0.0335569
    ## [1] "INSO_1-28-C"
    ## 
    ## Estimated effective doses
    ## 
    ##        Estimate Std. Error    Lower    Upper
    ## e:1:50 0.200379   0.020104 0.159429 0.241329
    ## [1] "INSO_1-28-D"
    ## 
    ## Estimated effective doses
    ## 
    ##        Estimate Std. Error    Lower    Upper
    ## e:1:50  0.30812    0.24033 -0.18142  0.79765
    ## [1] "INSO_1-52-B"
    ## 
    ## Estimated effective doses
    ## 
    ##        Estimate Std. Error    Lower    Upper
    ## e:1:50 0.227103   0.019697 0.186983 0.267224
    ## [1] "INSO_1-53A"
    ## 
    ## Estimated effective doses
    ## 
    ##        Estimate Std. Error   Lower   Upper
    ## e:1:50  0.20009    0.01448 0.17059 0.22958
    ## [1] "INSO_2-57"
    ## 
    ## Estimated effective doses
    ## 
    ##        Estimate Std. Error    Lower    Upper
    ## e:1:50 0.223966   0.058089 0.105642 0.342290
    ## [1] "INSO_3-45"
    ## 
    ## Estimated effective doses
    ## 
    ##        Estimate Std. Error    Lower    Upper
    ## e:1:50 0.288001   0.074597 0.136052 0.439951
    ## [1] "INSO_3-49"
    ## 
    ## Estimated effective doses
    ## 
    ##        Estimate Std. Error    Lower    Upper
    ## e:1:50 0.369422   0.077015 0.212549 0.526296
    ## [1] "IASO_1-16.1h"
    ## 
    ## Estimated effective doses
    ## 
    ##        Estimate Std. Error    Lower    Upper
    ## e:1:50 0.118335   0.011733 0.094404 0.142265
    ## [1] "IASO_1-16.2r"
    ## 
    ## Estimated effective doses
    ## 
    ##        Estimate Std. Error    Lower    Upper
    ## e:1:50 0.189945   0.013146 0.163097 0.216793
    ## [1] "IASO_1-20.44rt"
    ## 
    ## Estimated effective doses
    ## 
    ##         Estimate Std. Error     Lower     Upper
    ## e:1:50 0.0483296  0.0022658 0.0437143 0.0529448
    ## [1] "IASO_10-28.24rt"
    ## 
    ## Estimated effective doses
    ## 
    ##        Estimate Std. Error    Lower    Upper
    ## e:1:50 0.190146   0.027182 0.134779 0.245514
    ## [1] "IASO_2-11.8"
    ## 
    ## Estimated effective doses
    ## 
    ##        Estimate Std. Error   Lower   Upper
    ## e:1:50  0.16580    0.01082 0.14376 0.18784
    ## [1] "IASO_6-10.15h"
    ## 
    ## Estimated effective doses
    ## 
    ##        Estimate Std. Error    Lower    Upper
    ## e:1:50 0.183297   0.017237 0.148187 0.218407
    ## [1] "IASO_6-34.31r"
    ## 
    ## Estimated effective doses
    ## 
    ##        Estimate Std. Error    Lower    Upper
    ## e:1:50 0.130147   0.010705 0.108342 0.151951
    ## [1] "IASO_9-10.4h"
    ## 
    ## Estimated effective doses
    ## 
    ##         Estimate Std. Error     Lower     Upper
    ## e:1:50 0.1915200  0.0077369 0.1757605 0.2072795
    ## [1] "IASO_9-11.1h"
    ## 
    ## Estimated effective doses
    ## 
    ##        Estimate Std. Error    Lower    Upper
    ## e:1:50 0.123034   0.006696 0.109395 0.136673
    ## [1] "IASO_9-24.27rd"
    ## 
    ## Estimated effective doses
    ## 
    ##         Estimate Std. Error     Lower     Upper
    ## e:1:50 0.1935594  0.0094277 0.1743559 0.2127629
    ## [1] "IASO_9-29.33h"
    ## 
    ## Estimated effective doses
    ## 
    ##        Estimate Std. Error    Lower    Upper
    ## e:1:50 0.198000   0.019219 0.158853 0.237148
    ## [1] "IASO_9-31.37h"
    ## 
    ## Estimated effective doses
    ## 
    ##         Estimate Std. Error     Lower     Upper
    ## e:1:50 0.1114482  0.0070542 0.0970793 0.1258172
    ## [1] "IASO_9-36.42rd"
    ## 
    ## Estimated effective doses
    ## 
    ##        Estimate Std. Error    Lower    Upper
    ## e:1:50 0.159440   0.010423 0.138209 0.180671
    ## [1] "IASO_9-4.8h"
    ## 
    ## Estimated effective doses
    ## 
    ##         Estimate Std. Error     Lower     Upper
    ## e:1:50 0.1372654  0.0070847 0.1228343 0.1516965
    ## [1] "KSSO_3-34"
    ## 
    ## Estimated effective doses
    ## 
    ##         Estimate Std. Error     Lower     Upper
    ## e:1:50  0.427766   0.230327 -0.041395  0.896927
    ## [1] "KSSO_5-21"
    ## 
    ## Estimated effective doses
    ## 
    ##         Estimate Std. Error     Lower     Upper
    ## e:1:50 0.0991738  0.0040323 0.0909603 0.1073874
    ## [1] "C-MISO2_1-19"
    ## 
    ## Estimated effective doses
    ## 
    ##        Estimate Std. Error    Lower    Upper
    ## e:1:50 0.106855   0.022010 0.062022 0.151687
    ## [1] "MISO_5-9"
    ## 
    ## Estimated effective doses
    ## 
    ##        Estimate Std. Error    Lower    Upper
    ## e:1:50 0.156127   0.021551 0.112229 0.200025
    ## [1] "MISO_8-23"
    ## 
    ## Estimated effective doses
    ## 
    ##        Estimate Std. Error    Lower    Upper
    ## e:1:50 0.308127   0.019233 0.268951 0.347304
    ## [1] "C-MNSO_6-4"
    ## 
    ## Estimated effective doses
    ## 
    ##        Estimate Std. Error    Lower    Upper
    ## e:1:50 0.117014   0.012255 0.092052 0.141977
    ## [1] "C-MNSO2_1-1"
    ## 
    ## Estimated effective doses
    ## 
    ##        Estimate Std. Error    Lower    Upper
    ## e:1:50 0.177036   0.011915 0.152767 0.201305
    ## [1] "C-MNSO2_1-19"
    ## 
    ## Estimated effective doses
    ## 
    ##        Estimate Std. Error    Lower    Upper
    ## e:1:50 0.234268   0.017095 0.199447 0.269088
    ## [1] "C-MNSO2_2-10"
    ## 
    ## Estimated effective doses
    ## 
    ##         Estimate Std. Error     Lower     Upper
    ## e:1:50 0.0172659  0.0012838 0.0146508 0.0198809
    ## [1] "MNSO_2-11"
    ## 
    ## Estimated effective doses
    ## 
    ##        Estimate Std. Error    Lower    Upper
    ## e:1:50 0.201737   0.012113 0.176998 0.226476
    ## [1] "MNSO_2-31"
    ## 
    ## Estimated effective doses
    ## 
    ##        Estimate Std. Error    Lower    Upper
    ## e:1:50 0.306968   0.078617 0.146831 0.467105
    ## [1] "MNSO_2-52"
    ## 
    ## Estimated effective doses
    ## 
    ##        Estimate Std. Error    Lower    Upper
    ## e:1:50 0.289597   0.081347 0.123464 0.455730
    ## [1] "MNSO_5-20"
    ## 
    ## Estimated effective doses
    ## 
    ##        Estimate Std. Error    Lower    Upper
    ## e:1:50 0.213191   0.024013 0.164278 0.262104
    ## [1] "NESO_1-27"
    ## 
    ## Estimated effective doses
    ## 
    ##        Estimate Std. Error    Lower    Upper
    ## e:1:50  0.42728    0.28840 -0.16016  1.01472
    ## [1] "NESO_3-20"
    ## 
    ## Estimated effective doses
    ## 
    ##         Estimate Std. Error     Lower     Upper
    ## e:1:50 0.0900834  0.0021351 0.0857344 0.0944324
    ## [1] "NESO_4-20"
    ## 
    ## Estimated effective doses
    ## 
    ##         Estimate Std. Error     Lower     Upper
    ## e:1:50 0.1573077  0.0065037 0.1440602 0.1705553
    ## [1] "NESO_4-38"
    ## 
    ## Estimated effective doses
    ## 
    ##        Estimate Std. Error   Lower   Upper
    ## e:1:50  0.16319    0.01761 0.12732 0.19906
    ## [1] "NESO_4-40"
    ## 
    ## Estimated effective doses
    ## 
    ##        Estimate Std. Error   Lower   Upper
    ## e:1:50  0.20914    0.01403 0.18056 0.23772
    ## [1] "NESO_4-42"
    ## 
    ## Estimated effective doses
    ## 
    ##        Estimate Std. Error   Lower   Upper
    ## e:1:50  0.17905    0.00849 0.16171 0.19639
    ## [1] "NESO_4-47"
    ## 
    ## Estimated effective doses
    ## 
    ##         Estimate Std. Error     Lower     Upper
    ## e:1:50 0.1587569  0.0098007 0.1387411 0.1787727
    ## [1] "NDSO_4-1"
    ## 
    ## Estimated effective doses
    ## 
    ##         Estimate Std. Error     Lower     Upper
    ## e:1:50 0.1352667  0.0074545 0.1200824 0.1504511
    ## [1] "NDSO_4-18"
    ## 
    ## Estimated effective doses
    ## 
    ##        Estimate Std. Error    Lower    Upper
    ## e:1:50 0.247784   0.036714 0.173000 0.322567
    ## [1] "NDSO_4-2"
    ## 
    ## Estimated effective doses
    ## 
    ##        Estimate Std. Error    Lower    Upper
    ## e:1:50 0.235268   0.026532 0.181223 0.289313
    ## [1] "NDSO_4-43"
    ## 
    ## Estimated effective doses
    ## 
    ##        Estimate Std. Error    Lower    Upper
    ## e:1:50 0.066926   0.010213 0.046123 0.087728
    ## [1] "NDSO_4-45"
    ## 
    ## Estimated effective doses
    ## 
    ##        Estimate Std. Error    Lower    Upper
    ## e:1:50 0.174492   0.010501 0.153102 0.195882
    ## [1] "NDSO_5-22"
    ## 
    ## Estimated effective doses
    ## 
    ##        Estimate Std. Error    Lower    Upper
    ## e:1:50 0.181951   0.028336 0.124233 0.239669
    ## [1] "NDSO_5-36"
    ## 
    ## Estimated effective doses
    ## 
    ##        Estimate Std. Error    Lower    Upper
    ## e:1:50 0.195576   0.013476 0.168125 0.223027
    ## [1] "NDSO_5-46"
    ## 
    ## Estimated effective doses
    ## 
    ##        Estimate Std. Error    Lower    Upper
    ## e:1:50 0.168410   0.010795 0.146421 0.190399
    ## [1] "NDSO_5-49"
    ## 
    ## Estimated effective doses
    ## 
    ##         Estimate Std. Error     Lower     Upper
    ## e:1:50 0.1546980  0.0093702 0.1354373 0.1739588
    ## [1] "NDSO_5-9"
    ## 
    ## Estimated effective doses
    ## 
    ##        Estimate Std. Error    Lower    Upper
    ## e:1:50 0.162666   0.011066 0.140126 0.185206
    ## [1] "C-SDSO2_5-16"
    ## 
    ## Estimated effective doses
    ## 
    ##        Estimate Std. Error    Lower    Upper
    ## e:1:50 0.147113   0.008233 0.130343 0.163883
    ## [1] "C-SDSO2_5-17"
    ## 
    ## Estimated effective doses
    ## 
    ##         Estimate Std. Error     Lower     Upper
    ## e:1:50 0.1376907  0.0077899 0.1218232 0.1535582
    ## [1] "C-SDSO2_5-29"
    ## 
    ## Estimated effective doses
    ## 
    ##        Estimate Std. Error    Lower    Upper
    ## e:1:50 0.118886   0.004502 0.109716 0.128057
    ## [1] "C-SDSO2_5-8"
    ## 
    ## Estimated effective doses
    ## 
    ##        Estimate Std. Error    Lower    Upper
    ## e:1:50 0.206342   0.016866 0.171988 0.240696
    ## [1] "C-SDSO2_5-9"
    ## 
    ## Estimated effective doses
    ## 
    ##        Estimate Std. Error    Lower    Upper
    ## e:1:50 0.175509   0.013954 0.147086 0.203932
    ## [1] "C-SDSO2_6-33"
    ## 
    ## Estimated effective doses
    ## 
    ##        Estimate Std. Error    Lower    Upper
    ## e:1:50  0.65376    0.63282 -0.63525  1.94277
    ## [1] "V-SDSO2_5-41"
    ## 
    ## Estimated effective doses
    ## 
    ##        Estimate Std. Error    Lower    Upper
    ## e:1:50 0.211026   0.012571 0.185419 0.236633

``` r
    EC50.114 # display the dataset
```

    ##            nm..i..       EC50
    ## 1       ILSO_5-41c 0.10703185
    ## 2       ILSO_5-42c 0.24865540
    ## 3       ILSO_5-49b 0.16759162
    ## 4         ILSO_6-1 0.10826767
    ## 5       ILSO_6-12B 0.18427088
    ## 6        ILSO_6-2b 0.22743219
    ## 7       ILSO_6-33C 0.10186268
    ## 8       ILSO_6-39C 0.11027208
    ## 9       ILSO_6-15b 0.12328848
    ## 10      ILSO_6-28C 0.09987271
    ## 11      ILSO_6-34c 0.69464915
    ## 12      ILSO_6-35b 0.11397531
    ## 13      ILSO_6-36b 0.21743559
    ## 14      INSO_1-13D 0.14323325
    ## 15      INSO_1-17C 0.18335968
    ## 16      INSO_1-17D 0.18692904
    ## 17     INSO_1-23-C 0.02992881
    ## 18     INSO_1-28-C 0.20037911
    ## 19     INSO_1-28-D 0.30811657
    ## 20     INSO_1-52-B 0.22710347
    ## 21      INSO_1-53A 0.20008613
    ## 22       INSO_2-57 0.22396630
    ## 23       INSO_3-45 0.28800125
    ## 24       INSO_3-49 0.36942218
    ## 25    IASO_1-16.1h 0.11833479
    ## 26    IASO_1-16.2r 0.18994506
    ## 27  IASO_1-20.44rt 0.04832956
    ## 28 IASO_10-28.24rt 0.19014621
    ## 29     IASO_2-11.8 0.16580086
    ## 30   IASO_6-10.15h 0.18329731
    ## 31   IASO_6-34.31r 0.13014679
    ## 32    IASO_9-10.4h 0.19152001
    ## 33    IASO_9-11.1h 0.12303394
    ## 34  IASO_9-24.27rd 0.19355935
    ## 35   IASO_9-29.33h 0.19800048
    ## 36   IASO_9-31.37h 0.11144825
    ## 37  IASO_9-36.42rd 0.15944012
    ## 38     IASO_9-4.8h 0.13726542
    ## 39       KSSO_3-34 0.42776565
    ## 40       KSSO_5-21 0.09917381
    ## 41    C-MISO2_1-19 0.10685464
    ## 42        MISO_5-9 0.15612701
    ## 43       MISO_8-23 0.30812750
    ## 44      C-MNSO_6-4 0.11701436
    ## 45     C-MNSO2_1-1 0.17703620
    ## 46    C-MNSO2_1-19 0.23426773
    ## 47    C-MNSO2_2-10 0.01726587
    ## 48       MNSO_2-11 0.20173727
    ## 49       MNSO_2-31 0.30696808
    ## 50       MNSO_2-52 0.28959682
    ## 51       MNSO_5-20 0.21319109
    ## 52       NESO_1-27 0.42727958
    ## 53       NESO_3-20 0.09008340
    ## 54       NESO_4-20 0.15730773
    ## 55       NESO_4-38 0.16318698
    ## 56       NESO_4-40 0.20913713
    ## 57       NESO_4-42 0.17904661
    ## 58       NESO_4-47 0.15875693
    ## 59        NDSO_4-1 0.13526673
    ## 60       NDSO_4-18 0.24778376
    ## 61        NDSO_4-2 0.23526824
    ## 62       NDSO_4-43 0.06692569
    ## 63       NDSO_4-45 0.17449202
    ## 64       NDSO_5-22 0.18195115
    ## 65       NDSO_5-36 0.19557585
    ## 66       NDSO_5-46 0.16841047
    ## 67       NDSO_5-49 0.15469803
    ## 68        NDSO_5-9 0.16266600
    ## 69    C-SDSO2_5-16 0.14711258
    ## 70    C-SDSO2_5-17 0.13769070
    ## 71    C-SDSO2_5-29 0.11888637
    ## 72     C-SDSO2_5-8 0.20634225
    ## 73     C-SDSO2_5-9 0.17550901
    ## 74    C-SDSO2_6-33 0.65376130
    ## 75    V-SDSO2_5-41 0.21102570

### Using tidyverse map

``` r
#how to write for loop and append into the bottom
EC50.data %>%
  group_by(is) %>%
  nest() %>% #nest allows to make a sub-dataframe within a dataframe so that now we can loop over the data
  mutate(ll.4.mod = map(data, ~drm(.$relgrowth ~ .$conc, 
                              fct = LL.4(fixed = c(NA, NA, NA, NA), 
                                         names = c("Slope", "Lower", "Upper", "EC50"))))) %>% # we can now loop over the data, for loop contained within a function here. (period ".") symbol inherit all the data that is used in that iteration. This code create new column ll.4.mod that has summary output if drm function over our data and stored it in dataframe, map functions helps iterate through all the "data" for each nested group (data is the column within the sub dataframe for each isolate that was grouped)
  mutate(ec50 = map(ll.4.mod, ~ED(., 
                              respLev = c(50), 
                              type = "relative",
                              interval = "delta")[[1]])) %>% # to calculate ec50 value from each dataframe from the model
  unnest(ec50) #we can unnest the nested dataframe
```

    ## Warning: There were 19 warnings in `mutate()`.
    ## The first warning was:
    ## ℹ In argument: `ll.4.mod = map(...)`.
    ## ℹ In group 4: `is = "C-MNSO2_2-10"`.
    ## Caused by warning in `log()`:
    ## ! NaNs produced
    ## ℹ Run `dplyr::last_dplyr_warnings()` to see the 18 remaining warnings.

    ## 
    ## Estimated effective doses
    ## 
    ##        Estimate Std. Error    Lower    Upper
    ## e:1:50 0.106855   0.022010 0.062022 0.151687
    ## 
    ## Estimated effective doses
    ## 
    ##        Estimate Std. Error    Lower    Upper
    ## e:1:50 0.177036   0.011915 0.152767 0.201305
    ## 
    ## Estimated effective doses
    ## 
    ##        Estimate Std. Error    Lower    Upper
    ## e:1:50 0.234268   0.017095 0.199447 0.269088
    ## 
    ## Estimated effective doses
    ## 
    ##         Estimate Std. Error     Lower     Upper
    ## e:1:50 0.0172659  0.0012838 0.0146508 0.0198809
    ## 
    ## Estimated effective doses
    ## 
    ##        Estimate Std. Error    Lower    Upper
    ## e:1:50 0.117014   0.012255 0.092052 0.141977
    ## 
    ## Estimated effective doses
    ## 
    ##        Estimate Std. Error    Lower    Upper
    ## e:1:50 0.147113   0.008233 0.130343 0.163883
    ## 
    ## Estimated effective doses
    ## 
    ##         Estimate Std. Error     Lower     Upper
    ## e:1:50 0.1376907  0.0077899 0.1218232 0.1535582
    ## 
    ## Estimated effective doses
    ## 
    ##        Estimate Std. Error    Lower    Upper
    ## e:1:50 0.118886   0.004502 0.109716 0.128057
    ## 
    ## Estimated effective doses
    ## 
    ##        Estimate Std. Error    Lower    Upper
    ## e:1:50 0.206342   0.016866 0.171988 0.240696
    ## 
    ## Estimated effective doses
    ## 
    ##        Estimate Std. Error    Lower    Upper
    ## e:1:50 0.175509   0.013954 0.147086 0.203932
    ## 
    ## Estimated effective doses
    ## 
    ##        Estimate Std. Error    Lower    Upper
    ## e:1:50  0.65376    0.63282 -0.63525  1.94277
    ## 
    ## Estimated effective doses
    ## 
    ##        Estimate Std. Error    Lower    Upper
    ## e:1:50 0.118335   0.011733 0.094404 0.142265
    ## 
    ## Estimated effective doses
    ## 
    ##        Estimate Std. Error    Lower    Upper
    ## e:1:50 0.189945   0.013146 0.163097 0.216793
    ## 
    ## Estimated effective doses
    ## 
    ##         Estimate Std. Error     Lower     Upper
    ## e:1:50 0.0483296  0.0022658 0.0437143 0.0529448
    ## 
    ## Estimated effective doses
    ## 
    ##        Estimate Std. Error    Lower    Upper
    ## e:1:50 0.190146   0.027182 0.134779 0.245514
    ## 
    ## Estimated effective doses
    ## 
    ##        Estimate Std. Error   Lower   Upper
    ## e:1:50  0.16580    0.01082 0.14376 0.18784
    ## 
    ## Estimated effective doses
    ## 
    ##        Estimate Std. Error    Lower    Upper
    ## e:1:50 0.183297   0.017237 0.148187 0.218407
    ## 
    ## Estimated effective doses
    ## 
    ##        Estimate Std. Error    Lower    Upper
    ## e:1:50 0.130147   0.010705 0.108342 0.151951
    ## 
    ## Estimated effective doses
    ## 
    ##         Estimate Std. Error     Lower     Upper
    ## e:1:50 0.1915200  0.0077369 0.1757605 0.2072795
    ## 
    ## Estimated effective doses
    ## 
    ##        Estimate Std. Error    Lower    Upper
    ## e:1:50 0.123034   0.006696 0.109395 0.136673
    ## 
    ## Estimated effective doses
    ## 
    ##         Estimate Std. Error     Lower     Upper
    ## e:1:50 0.1935594  0.0094277 0.1743559 0.2127629
    ## 
    ## Estimated effective doses
    ## 
    ##        Estimate Std. Error    Lower    Upper
    ## e:1:50 0.198000   0.019219 0.158853 0.237148
    ## 
    ## Estimated effective doses
    ## 
    ##         Estimate Std. Error     Lower     Upper
    ## e:1:50 0.1114482  0.0070542 0.0970793 0.1258172
    ## 
    ## Estimated effective doses
    ## 
    ##        Estimate Std. Error    Lower    Upper
    ## e:1:50 0.159440   0.010423 0.138209 0.180671
    ## 
    ## Estimated effective doses
    ## 
    ##         Estimate Std. Error     Lower     Upper
    ## e:1:50 0.1372654  0.0070847 0.1228343 0.1516965
    ## 
    ## Estimated effective doses
    ## 
    ##         Estimate Std. Error     Lower     Upper
    ## e:1:50 0.1070318  0.0055365 0.0957543 0.1183094
    ## 
    ## Estimated effective doses
    ## 
    ##        Estimate Std. Error    Lower    Upper
    ## e:1:50 0.248655   0.028485 0.190633 0.306678
    ## 
    ## Estimated effective doses
    ## 
    ##        Estimate Std. Error    Lower    Upper
    ## e:1:50 0.167592   0.010197 0.146821 0.188362
    ## 
    ## Estimated effective doses
    ## 
    ##         Estimate Std. Error     Lower     Upper
    ## e:1:50 0.1082677  0.0051459 0.0977858 0.1187495
    ## 
    ## Estimated effective doses
    ## 
    ##        Estimate Std. Error    Lower    Upper
    ## e:1:50 0.184271   0.036047 0.110846 0.257695
    ## 
    ## Estimated effective doses
    ## 
    ##        Estimate Std. Error    Lower    Upper
    ## e:1:50 0.123288   0.014018 0.094735 0.151841
    ## 
    ## Estimated effective doses
    ## 
    ##         Estimate Std. Error     Lower     Upper
    ## e:1:50 0.0998727  0.0044787 0.0907498 0.1089956
    ## 
    ## Estimated effective doses
    ## 
    ##        Estimate Std. Error    Lower    Upper
    ## e:1:50 0.227432   0.040614 0.144704 0.310160
    ## 
    ## Estimated effective doses
    ## 
    ##        Estimate Std. Error    Lower    Upper
    ## e:1:50 0.101863   0.003487 0.094760 0.108965
    ## 
    ## Estimated effective doses
    ## 
    ##        Estimate Std. Error    Lower    Upper
    ## e:1:50  0.69465    0.39164 -0.10310  1.49240
    ## 
    ## Estimated effective doses
    ## 
    ##        Estimate Std. Error    Lower    Upper
    ## e:1:50 0.113975   0.012773 0.087958 0.139993
    ## 
    ## Estimated effective doses
    ## 
    ##        Estimate Std. Error    Lower    Upper
    ## e:1:50 0.217436   0.027934 0.160536 0.274335
    ## 
    ## Estimated effective doses
    ## 
    ##         Estimate Std. Error     Lower     Upper
    ## e:1:50 0.1102721  0.0033354 0.1034780 0.1170661
    ## 
    ## Estimated effective doses
    ## 
    ##         Estimate Std. Error     Lower     Upper
    ## e:1:50 0.1432333  0.0093132 0.1242629 0.1622036
    ## 
    ## Estimated effective doses
    ## 
    ##        Estimate Std. Error   Lower   Upper
    ## e:1:50  0.18336    0.01293 0.15695 0.20977
    ## 
    ## Estimated effective doses
    ## 
    ##        Estimate Std. Error    Lower    Upper
    ## e:1:50 0.186929   0.034023 0.117626 0.256232
    ## 
    ## Estimated effective doses
    ## 
    ##         Estimate Std. Error     Lower     Upper
    ## e:1:50 0.0299288  0.0017812 0.0263007 0.0335569
    ## 
    ## Estimated effective doses
    ## 
    ##        Estimate Std. Error    Lower    Upper
    ## e:1:50 0.200379   0.020104 0.159429 0.241329
    ## 
    ## Estimated effective doses
    ## 
    ##        Estimate Std. Error    Lower    Upper
    ## e:1:50  0.30812    0.24033 -0.18142  0.79765
    ## 
    ## Estimated effective doses
    ## 
    ##        Estimate Std. Error    Lower    Upper
    ## e:1:50 0.227103   0.019697 0.186983 0.267224
    ## 
    ## Estimated effective doses
    ## 
    ##        Estimate Std. Error   Lower   Upper
    ## e:1:50  0.20009    0.01448 0.17059 0.22958
    ## 
    ## Estimated effective doses
    ## 
    ##        Estimate Std. Error    Lower    Upper
    ## e:1:50 0.223966   0.058089 0.105642 0.342290
    ## 
    ## Estimated effective doses
    ## 
    ##        Estimate Std. Error    Lower    Upper
    ## e:1:50 0.288001   0.074597 0.136052 0.439951
    ## 
    ## Estimated effective doses
    ## 
    ##        Estimate Std. Error    Lower    Upper
    ## e:1:50 0.369422   0.077015 0.212549 0.526296
    ## 
    ## Estimated effective doses
    ## 
    ##         Estimate Std. Error     Lower     Upper
    ## e:1:50  0.427766   0.230327 -0.041395  0.896927
    ## 
    ## Estimated effective doses
    ## 
    ##         Estimate Std. Error     Lower     Upper
    ## e:1:50 0.0991738  0.0040323 0.0909603 0.1073874
    ## 
    ## Estimated effective doses
    ## 
    ##        Estimate Std. Error    Lower    Upper
    ## e:1:50 0.156127   0.021551 0.112229 0.200025
    ## 
    ## Estimated effective doses
    ## 
    ##        Estimate Std. Error    Lower    Upper
    ## e:1:50 0.308127   0.019233 0.268951 0.347304
    ## 
    ## Estimated effective doses
    ## 
    ##        Estimate Std. Error    Lower    Upper
    ## e:1:50 0.201737   0.012113 0.176998 0.226476
    ## 
    ## Estimated effective doses
    ## 
    ##        Estimate Std. Error    Lower    Upper
    ## e:1:50 0.306968   0.078617 0.146831 0.467105
    ## 
    ## Estimated effective doses
    ## 
    ##        Estimate Std. Error    Lower    Upper
    ## e:1:50 0.289597   0.081347 0.123464 0.455730
    ## 
    ## Estimated effective doses
    ## 
    ##        Estimate Std. Error    Lower    Upper
    ## e:1:50 0.213191   0.024013 0.164278 0.262104
    ## 
    ## Estimated effective doses
    ## 
    ##         Estimate Std. Error     Lower     Upper
    ## e:1:50 0.1352667  0.0074545 0.1200824 0.1504511
    ## 
    ## Estimated effective doses
    ## 
    ##        Estimate Std. Error    Lower    Upper
    ## e:1:50 0.247784   0.036714 0.173000 0.322567
    ## 
    ## Estimated effective doses
    ## 
    ##        Estimate Std. Error    Lower    Upper
    ## e:1:50 0.235268   0.026532 0.181223 0.289313
    ## 
    ## Estimated effective doses
    ## 
    ##        Estimate Std. Error    Lower    Upper
    ## e:1:50 0.066926   0.010213 0.046123 0.087728
    ## 
    ## Estimated effective doses
    ## 
    ##        Estimate Std. Error    Lower    Upper
    ## e:1:50 0.174492   0.010501 0.153102 0.195882
    ## 
    ## Estimated effective doses
    ## 
    ##        Estimate Std. Error    Lower    Upper
    ## e:1:50 0.181951   0.028336 0.124233 0.239669
    ## 
    ## Estimated effective doses
    ## 
    ##        Estimate Std. Error    Lower    Upper
    ## e:1:50 0.195576   0.013476 0.168125 0.223027
    ## 
    ## Estimated effective doses
    ## 
    ##        Estimate Std. Error    Lower    Upper
    ## e:1:50 0.168410   0.010795 0.146421 0.190399
    ## 
    ## Estimated effective doses
    ## 
    ##         Estimate Std. Error     Lower     Upper
    ## e:1:50 0.1546980  0.0093702 0.1354373 0.1739588
    ## 
    ## Estimated effective doses
    ## 
    ##        Estimate Std. Error    Lower    Upper
    ## e:1:50 0.162666   0.011066 0.140126 0.185206
    ## 
    ## Estimated effective doses
    ## 
    ##        Estimate Std. Error    Lower    Upper
    ## e:1:50  0.42728    0.28840 -0.16017  1.01472
    ## 
    ## Estimated effective doses
    ## 
    ##         Estimate Std. Error     Lower     Upper
    ## e:1:50 0.0900834  0.0021351 0.0857344 0.0944324
    ## 
    ## Estimated effective doses
    ## 
    ##         Estimate Std. Error     Lower     Upper
    ## e:1:50 0.1573077  0.0065037 0.1440602 0.1705553
    ## 
    ## Estimated effective doses
    ## 
    ##        Estimate Std. Error   Lower   Upper
    ## e:1:50  0.16319    0.01761 0.12732 0.19906
    ## 
    ## Estimated effective doses
    ## 
    ##        Estimate Std. Error   Lower   Upper
    ## e:1:50  0.20914    0.01403 0.18056 0.23772
    ## 
    ## Estimated effective doses
    ## 
    ##        Estimate Std. Error   Lower   Upper
    ## e:1:50  0.17905    0.00849 0.16171 0.19639
    ## 
    ## Estimated effective doses
    ## 
    ##         Estimate Std. Error     Lower     Upper
    ## e:1:50 0.1587569  0.0098007 0.1387411 0.1787727
    ## 
    ## Estimated effective doses
    ## 
    ##        Estimate Std. Error    Lower    Upper
    ## e:1:50 0.211026   0.012571 0.185419 0.236633

    ## # A tibble: 75 × 4
    ## # Groups:   is [75]
    ##    is         data               ll.4.mod   ec50
    ##    <chr>      <list>             <list>    <dbl>
    ##  1 ILSO_5-41c <tibble [36 × 11]> <drc>    0.107 
    ##  2 ILSO_5-42c <tibble [36 × 11]> <drc>    0.249 
    ##  3 ILSO_5-49b <tibble [36 × 11]> <drc>    0.168 
    ##  4 ILSO_6-1   <tibble [36 × 11]> <drc>    0.108 
    ##  5 ILSO_6-12B <tibble [36 × 11]> <drc>    0.184 
    ##  6 ILSO_6-2b  <tibble [36 × 11]> <drc>    0.227 
    ##  7 ILSO_6-33C <tibble [36 × 11]> <drc>    0.102 
    ##  8 ILSO_6-39C <tibble [36 × 11]> <drc>    0.110 
    ##  9 ILSO_6-15b <tibble [36 × 11]> <drc>    0.123 
    ## 10 ILSO_6-28C <tibble [36 × 11]> <drc>    0.0999
    ## # ℹ 65 more rows
