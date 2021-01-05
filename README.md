
# Iraceplot

<!-- badges: start -->
<!-- badges: end -->

The goal of iraceplot is to generate various types of graphs that help to
better understand the data generated by irace

## Install Iraceplot

For installing iraceplot you need to install the devtools package:

``` r
install.packages("devtools")
```
Currently, the Irace Studio package can be installed from Gtihub:

``` r
devtools::install_github("pabloOnate/iraceplot")
```

## How To Use

This is a basic example which shows you how to solve a common problem:

``` r
library(iraceplot)
```

you need to have the file generated by irace de rdata loaded, you must replace the path of the file with yours

``` r
load("~/patch/example/name.Rdata")
```

The 'ibp()' function returns a graphic of box plot

``` r
ibp(iraceResults,numberInteraction,fileName)
```

Example 1

``` r
ibp(iraceResults)
Return the box plot of the last iteration of la elite configuration
```

Example 2

The following line allows us to visualize the number of iterations and the best configurations of each one
``` r
iraceResults$allElites
```

If I get a range of iterations that goes from 1 to 10 then I can choose which iteration to plot

``` r
ibp(iraceResults,3)
Return the box plot of the third iteration of la elite configuration

```

Example 3

Option 1:

``` r
ibp(iraceResults,2,"filename")
Return the box plot of the second iteration of la elite configuration, but it is saved directly to pdf file in current directory
```

Option 2:

``` r
ibp(iraceResults,2,"~/patch/example/filename")
Return the box plot of the second iteration of la elite configuration, but it is saved directly to a pdf file
```
