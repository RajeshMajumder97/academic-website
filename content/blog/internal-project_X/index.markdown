---
date: "2022-06-19T00:00:00Z"
external_link: ""
image:
#  caption: Photo by rawpixel on Unsplash
  focal_point: Smart
  
#slides: example
summary: The c3 package is a wrapper, or htmlwidget, for the C3 javascript charting library by Masayuki Tanaka. 

tags:
- Blogs
title: C3
categories: ["R"]
output:
  blogdown::html_page:
    toc: true
      
---

<script src="{{< blogdown/postref >}}index_files/htmlwidgets/htmlwidgets.js"></script>
<script src="{{< blogdown/postref >}}index_files/d3/d3.min.js"></script>
<link href="{{< blogdown/postref >}}index_files/c3/c3.min.css" rel="stylesheet" />
<script src="{{< blogdown/postref >}}index_files/c3/c3.min.js"></script>
<script src="{{< blogdown/postref >}}index_files/c3-binding/c3.js"></script>
<script src="{{< blogdown/postref >}}index_files/htmlwidgets/htmlwidgets.js"></script>
<script src="{{< blogdown/postref >}}index_files/d3/d3.min.js"></script>
<link href="{{< blogdown/postref >}}index_files/c3/c3.min.css" rel="stylesheet" />
<script src="{{< blogdown/postref >}}index_files/c3/c3.min.js"></script>
<script src="{{< blogdown/postref >}}index_files/c3-binding/c3.js"></script>
<script src="{{< blogdown/postref >}}index_files/htmlwidgets/htmlwidgets.js"></script>
<script src="{{< blogdown/postref >}}index_files/d3/d3.min.js"></script>
<link href="{{< blogdown/postref >}}index_files/c3/c3.min.css" rel="stylesheet" />
<script src="{{< blogdown/postref >}}index_files/c3/c3.min.js"></script>
<script src="{{< blogdown/postref >}}index_files/c3-binding/c3.js"></script>
<script src="{{< blogdown/postref >}}index_files/htmlwidgets/htmlwidgets.js"></script>
<script src="{{< blogdown/postref >}}index_files/d3/d3.min.js"></script>
<link href="{{< blogdown/postref >}}index_files/c3/c3.min.css" rel="stylesheet" />
<script src="{{< blogdown/postref >}}index_files/c3/c3.min.js"></script>
<script src="{{< blogdown/postref >}}index_files/c3-binding/c3.js"></script>
<script src="{{< blogdown/postref >}}index_files/htmlwidgets/htmlwidgets.js"></script>
<script src="{{< blogdown/postref >}}index_files/d3/d3.min.js"></script>
<link href="{{< blogdown/postref >}}index_files/c3/c3.min.css" rel="stylesheet" />
<script src="{{< blogdown/postref >}}index_files/c3/c3.min.js"></script>
<script src="{{< blogdown/postref >}}index_files/c3-binding/c3.js"></script>
<script src="{{< blogdown/postref >}}index_files/htmlwidgets/htmlwidgets.js"></script>
<script src="{{< blogdown/postref >}}index_files/d3/d3.min.js"></script>
<link href="{{< blogdown/postref >}}index_files/c3/c3.min.css" rel="stylesheet" />
<script src="{{< blogdown/postref >}}index_files/c3/c3.min.js"></script>
<script src="{{< blogdown/postref >}}index_files/c3-binding/c3.js"></script>
<script src="{{< blogdown/postref >}}index_files/htmlwidgets/htmlwidgets.js"></script>
<script src="{{< blogdown/postref >}}index_files/d3/d3.min.js"></script>
<link href="{{< blogdown/postref >}}index_files/c3/c3.min.css" rel="stylesheet" />
<script src="{{< blogdown/postref >}}index_files/c3/c3.min.js"></script>
<script src="{{< blogdown/postref >}}index_files/c3-binding/c3.js"></script>
<script src="{{< blogdown/postref >}}index_files/htmlwidgets/htmlwidgets.js"></script>
<script src="{{< blogdown/postref >}}index_files/d3/d3.min.js"></script>
<link href="{{< blogdown/postref >}}index_files/c3/c3.min.css" rel="stylesheet" />
<script src="{{< blogdown/postref >}}index_files/c3/c3.min.js"></script>
<script src="{{< blogdown/postref >}}index_files/c3-binding/c3.js"></script>
<script src="{{< blogdown/postref >}}index_files/htmlwidgets/htmlwidgets.js"></script>
<script src="{{< blogdown/postref >}}index_files/d3/d3.min.js"></script>
<link href="{{< blogdown/postref >}}index_files/c3/c3.min.css" rel="stylesheet" />
<script src="{{< blogdown/postref >}}index_files/c3/c3.min.js"></script>
<script src="{{< blogdown/postref >}}index_files/c3-binding/c3.js"></script>
<script src="{{< blogdown/postref >}}index_files/htmlwidgets/htmlwidgets.js"></script>
<script src="{{< blogdown/postref >}}index_files/d3/d3.min.js"></script>
<link href="{{< blogdown/postref >}}index_files/c3/c3.min.css" rel="stylesheet" />
<script src="{{< blogdown/postref >}}index_files/c3/c3.min.js"></script>
<script src="{{< blogdown/postref >}}index_files/c3-binding/c3.js"></script>
<script src="{{< blogdown/postref >}}index_files/htmlwidgets/htmlwidgets.js"></script>
<script src="{{< blogdown/postref >}}index_files/d3/d3.min.js"></script>
<link href="{{< blogdown/postref >}}index_files/c3/c3.min.css" rel="stylesheet" />
<script src="{{< blogdown/postref >}}index_files/c3/c3.min.js"></script>
<script src="{{< blogdown/postref >}}index_files/c3-binding/c3.js"></script>
<script src="{{< blogdown/postref >}}index_files/htmlwidgets/htmlwidgets.js"></script>
<script src="{{< blogdown/postref >}}index_files/d3/d3.min.js"></script>
<link href="{{< blogdown/postref >}}index_files/c3/c3.min.css" rel="stylesheet" />
<script src="{{< blogdown/postref >}}index_files/c3/c3.min.js"></script>
<script src="{{< blogdown/postref >}}index_files/c3-binding/c3.js"></script>
<script src="{{< blogdown/postref >}}index_files/htmlwidgets/htmlwidgets.js"></script>
<script src="{{< blogdown/postref >}}index_files/d3/d3.min.js"></script>
<link href="{{< blogdown/postref >}}index_files/c3/c3.min.css" rel="stylesheet" />
<script src="{{< blogdown/postref >}}index_files/c3/c3.min.js"></script>
<script src="{{< blogdown/postref >}}index_files/c3-binding/c3.js"></script>
<script src="{{< blogdown/postref >}}index_files/htmlwidgets/htmlwidgets.js"></script>
<script src="{{< blogdown/postref >}}index_files/d3/d3.min.js"></script>
<link href="{{< blogdown/postref >}}index_files/c3/c3.min.css" rel="stylesheet" />
<script src="{{< blogdown/postref >}}index_files/c3/c3.min.js"></script>
<script src="{{< blogdown/postref >}}index_files/c3-binding/c3.js"></script>
<script src="{{< blogdown/postref >}}index_files/htmlwidgets/htmlwidgets.js"></script>
<script src="{{< blogdown/postref >}}index_files/d3/d3.min.js"></script>
<link href="{{< blogdown/postref >}}index_files/c3/c3.min.css" rel="stylesheet" />
<script src="{{< blogdown/postref >}}index_files/c3/c3.min.js"></script>
<script src="{{< blogdown/postref >}}index_files/c3-binding/c3.js"></script>
<script src="{{< blogdown/postref >}}index_files/htmlwidgets/htmlwidgets.js"></script>
<script src="{{< blogdown/postref >}}index_files/d3/d3.min.js"></script>
<link href="{{< blogdown/postref >}}index_files/c3/c3.min.css" rel="stylesheet" />
<script src="{{< blogdown/postref >}}index_files/c3/c3.min.js"></script>
<script src="{{< blogdown/postref >}}index_files/c3-binding/c3.js"></script>
<script src="{{< blogdown/postref >}}index_files/htmlwidgets/htmlwidgets.js"></script>
<script src="{{< blogdown/postref >}}index_files/d3/d3.min.js"></script>
<link href="{{< blogdown/postref >}}index_files/c3/c3.min.css" rel="stylesheet" />
<script src="{{< blogdown/postref >}}index_files/c3/c3.min.js"></script>
<script src="{{< blogdown/postref >}}index_files/c3-binding/c3.js"></script>
<script src="{{< blogdown/postref >}}index_files/htmlwidgets/htmlwidgets.js"></script>
<script src="{{< blogdown/postref >}}index_files/d3/d3.min.js"></script>
<link href="{{< blogdown/postref >}}index_files/c3/c3.min.css" rel="stylesheet" />
<script src="{{< blogdown/postref >}}index_files/c3/c3.min.js"></script>
<script src="{{< blogdown/postref >}}index_files/c3-binding/c3.js"></script>

The `c3` package is a wrapper, or htmlwidget, for the C3 javascript charting library by Masayuki Tanaka. You will find this package useful if you are wanting to create a chart using R and embedding it in a Rmarkdown document or Shiny App.

The `C3` library is very versatile and includes a lot of options. Currently this package wraps most of the `C3` options object. Even with this current limitation a wide range of options are available.

## Instalation

``` r
install.packages("c3")

# or

devtools::install_github("mrjoh3/c3")
```

## Usage

The `c3` package is intended to be as simple and lightweight as possible. As a starting point the data input must be a `data.frame` or `tibble` with several options.

-   If a `data.frame` without any options is passed all of the numeric columns will be plotted. This can be used in line and bar plots. Each column is a line or bar.

-   For more complex plots only 3 columns are used, those defined as `x`, `y` and `group`. This requires a `data.frame` with a vertical structure.

### The Basics

Where no options are supplied a simple line plot is produced by default. Where no x-axis is defined the plots are sequential. `Date` x-axis can be parsed with not additional setting if in the format `%Y-%m-%d` (ie ‘2014-01-01’)

``` r
library(c3)
```

    ## Warning: package 'c3' was built under R version 4.1.3

    ## 
    ## Attaching package: 'c3'

    ## The following objects are masked from 'package:graphics':
    ## 
    ##     grid, legend

``` r
data = data.frame(a = abs(rnorm(20) * 10),
                  b = abs(rnorm(20) * 10),
                  date = seq(as.Date("2011-01-01"), by = "month", length.out = 20))
c3(data)
```

<div id="htmlwidget-1" style="width:672px;height:480px;" class="c3 html-widget"></div>
<script type="application/json" data-for="htmlwidget-1">{"x":{"data":{"json":[{"a":7.711,"b":0.9687},{"a":2.8013,"b":6.1846},{"a":1.8475,"b":10.0767},{"a":27.6863,"b":12.2308},{"a":12.3611,"b":7.0573},{"a":12.4269,"b":1.293},{"a":18.5765,"b":3.4815},{"a":9.1967,"b":14.4533},{"a":0.2613,"b":3.1618},{"a":3.1556,"b":9.6671},{"a":14.3516,"b":1.6119},{"a":12.755,"b":4.4683},{"a":20.1429,"b":5.7593},{"a":5.3441,"b":2.0097},{"a":6.2215,"b":15.8212},{"a":1.0995,"b":4.1461},{"a":11.7984,"b":5.9374},{"a":16.2198,"b":18.904},{"a":11.6513,"b":15.6244},{"a":11.3397,"b":6.1114}],"keys":{"value":["a","b"]}},"opts":{"x":null,"y":null,"types":{"a":"numeric","b":"numeric","date":"Date"}}},"evals":[],"jsHooks":[]}</script>

### Piping

The package also imports the magrittr piping function `(%>%)` to simplify syntax.

``` r
data%>%c3()
```

<div id="htmlwidget-2" style="width:672px;height:480px;" class="c3 html-widget"></div>
<script type="application/json" data-for="htmlwidget-2">{"x":{"data":{"json":[{"a":7.711,"b":0.9687},{"a":2.8013,"b":6.1846},{"a":1.8475,"b":10.0767},{"a":27.6863,"b":12.2308},{"a":12.3611,"b":7.0573},{"a":12.4269,"b":1.293},{"a":18.5765,"b":3.4815},{"a":9.1967,"b":14.4533},{"a":0.2613,"b":3.1618},{"a":3.1556,"b":9.6671},{"a":14.3516,"b":1.6119},{"a":12.755,"b":4.4683},{"a":20.1429,"b":5.7593},{"a":5.3441,"b":2.0097},{"a":6.2215,"b":15.8212},{"a":1.0995,"b":4.1461},{"a":11.7984,"b":5.9374},{"a":16.2198,"b":18.904},{"a":11.6513,"b":15.6244},{"a":11.3397,"b":6.1114}],"keys":{"value":["a","b"]}},"opts":{"x":null,"y":null,"types":{"a":"numeric","b":"numeric","date":"Date"}}},"evals":[],"jsHooks":[]}</script>

## Other Line Plots

There are 5 different line plots available:

-   line
-   spline
-   step
-   area
-   area-step

### Spline

``` r
data %>%
  c3() %>%
  c3_line('spline')
```

<div id="htmlwidget-3" style="width:672px;height:480px;" class="c3 html-widget"></div>
<script type="application/json" data-for="htmlwidget-3">{"x":{"data":{"json":[{"a":7.711,"b":0.9687},{"a":2.8013,"b":6.1846},{"a":1.8475,"b":10.0767},{"a":27.6863,"b":12.2308},{"a":12.3611,"b":7.0573},{"a":12.4269,"b":1.293},{"a":18.5765,"b":3.4815},{"a":9.1967,"b":14.4533},{"a":0.2613,"b":3.1618},{"a":3.1556,"b":9.6671},{"a":14.3516,"b":1.6119},{"a":12.755,"b":4.4683},{"a":20.1429,"b":5.7593},{"a":5.3441,"b":2.0097},{"a":6.2215,"b":15.8212},{"a":1.0995,"b":4.1461},{"a":11.7984,"b":5.9374},{"a":16.2198,"b":18.904},{"a":11.6513,"b":15.6244},{"a":11.3397,"b":6.1114}],"keys":{"value":["a","b"]},"type":"spline"},"opts":{"x":null,"y":null,"types":{"a":"numeric","b":"numeric","date":"Date"}}},"evals":[],"jsHooks":[]}</script>

### Step

``` r
data %>%
  c3(x = 'date') %>%
  c3_line('area-step')
```

<div id="htmlwidget-4" style="width:672px;height:480px;" class="c3 html-widget"></div>
<script type="application/json" data-for="htmlwidget-4">{"x":{"data":{"x":"date","json":[{"date":"2011-01-01","a":7.711,"b":0.9687},{"date":"2011-02-01","a":2.8013,"b":6.1846},{"date":"2011-03-01","a":1.8475,"b":10.0767},{"date":"2011-04-01","a":27.6863,"b":12.2308},{"date":"2011-05-01","a":12.3611,"b":7.0573},{"date":"2011-06-01","a":12.4269,"b":1.293},{"date":"2011-07-01","a":18.5765,"b":3.4815},{"date":"2011-08-01","a":9.1967,"b":14.4533},{"date":"2011-09-01","a":0.2613,"b":3.1618},{"date":"2011-10-01","a":3.1556,"b":9.6671},{"date":"2011-11-01","a":14.3516,"b":1.6119},{"date":"2011-12-01","a":12.755,"b":4.4683},{"date":"2012-01-01","a":20.1429,"b":5.7593},{"date":"2012-02-01","a":5.3441,"b":2.0097},{"date":"2012-03-01","a":6.2215,"b":15.8212},{"date":"2012-04-01","a":1.0995,"b":4.1461},{"date":"2012-05-01","a":11.7984,"b":5.9374},{"date":"2012-06-01","a":16.2198,"b":18.904},{"date":"2012-07-01","a":11.6513,"b":15.6244},{"date":"2012-08-01","a":11.3397,"b":6.1114}],"keys":{"value":["date","a","b"]},"type":"area-step"},"opts":{"x":"date","y":null,"types":{"a":"numeric","b":"numeric","date":"Date"}},"axis":{"x":{"label":"date","type":"timeseries"}}},"evals":[],"jsHooks":[]}</script>

## Bar Plots

``` r
data[1:10, ] %>%
  c3() %>%
  c3_bar(stacked = TRUE, 
         rotate = TRUE)
```

<div id="htmlwidget-5" style="width:672px;height:480px;" class="c3 html-widget"></div>
<script type="application/json" data-for="htmlwidget-5">{"x":{"data":{"json":[{"a":7.711,"b":0.9687},{"a":2.8013,"b":6.1846},{"a":1.8475,"b":10.0767},{"a":27.6863,"b":12.2308},{"a":12.3611,"b":7.0573},{"a":12.4269,"b":1.293},{"a":18.5765,"b":3.4815},{"a":9.1967,"b":14.4533},{"a":0.2613,"b":3.1618},{"a":3.1556,"b":9.6671}],"keys":{"value":["a","b"]},"type":"bar","groups":{"value":["a","b"]}},"opts":{"x":null,"y":null,"types":{"a":"numeric","b":"numeric","date":"Date"}},"axis":{"x":{"type":"category"},"rotated":true},"bar":{"zerobased":true,"width":{"ratio":0.6}}},"evals":[],"jsHooks":[]}</script>

## Mixed Geometry Plots

Mixed geometry currently only works with a horizontal `data.frame` where each numeric column is plotted.

``` r
data$c <- abs(rnorm(20) *10)
data$d <- abs(rnorm(20) *10)
data %>%
  c3() %>%
  c3_mixedGeom(type = 'bar', 
               stacked = c('b','d'),
               types = list(a='area',
                            c='spline')
               )
```

<div id="htmlwidget-6" style="width:672px;height:480px;" class="c3 html-widget"></div>
<script type="application/json" data-for="htmlwidget-6">{"x":{"data":{"json":[{"a":7.711,"b":0.9687,"c":3.4713,"d":12.656},{"a":2.8013,"b":6.1846,"c":8.2034,"d":12.205},{"a":1.8475,"b":10.0767,"c":16.5868,"d":20.0832},{"a":27.6863,"b":12.2308,"c":2.4936,"d":11.2891},{"a":12.3611,"b":7.0573,"c":10.6482,"d":12.2041},{"a":12.4269,"b":1.293,"c":3.7988,"d":6.1088},{"a":18.5765,"b":3.4815,"c":2.1802,"d":2.8879},{"a":9.1967,"b":14.4533,"c":8.3901,"d":3.1968},{"a":0.2613,"b":3.1618,"c":7.9922,"d":1.2813},{"a":3.1556,"b":9.6671,"c":10.4449,"d":12.0721},{"a":14.3516,"b":1.6119,"c":13.5387,"d":9.4406},{"a":12.755,"b":4.4683,"c":12.5018,"d":8.9714},{"a":20.1429,"b":5.7593,"c":9.9551,"d":5.182},{"a":5.3441,"b":2.0097,"c":15.0356,"d":0.8256},{"a":6.2215,"b":15.8212,"c":1.7341,"d":8.7247},{"a":1.0995,"b":4.1461,"c":9.2292,"d":9.2168},{"a":11.7984,"b":5.9374,"c":8.4761,"d":1.2355},{"a":16.2198,"b":18.904,"c":3.404,"d":12.0234},{"a":11.6513,"b":15.6244,"c":7.1839,"d":16.2478},{"a":11.3397,"b":6.1114,"c":13.8531,"d":5.6429}],"keys":{"value":["a","b","c","d"]},"type":"bar","types":{"a":"area","c":"spline"},"groups":["b","d"]},"opts":{"x":null,"y":null,"types":{"a":"numeric","b":"numeric","date":"Date","c":"numeric","d":"numeric"}}},"evals":[],"jsHooks":[]}</script>

## Secondary Y Axis

To use a secondary Y axis columns must first be matched to an axis and then the secondary axis made visible.

``` r
data %>% 
  dplyr::select(date, a, b) %>%
  c3(x = 'date',
     axes = list(a = 'y',
                 b = 'y2')) %>% 
  c3_mixedGeom(types = list(a = 'line',
                            b = 'area')) %>% 
  y2Axis()
```

<div id="htmlwidget-7" style="width:672px;height:480px;" class="c3 html-widget"></div>
<script type="application/json" data-for="htmlwidget-7">{"x":{"data":{"axes":{"a":"y","b":"y2"},"x":"date","json":[{"date":"2011-01-01","a":7.711,"b":0.9687},{"date":"2011-02-01","a":2.8013,"b":6.1846},{"date":"2011-03-01","a":1.8475,"b":10.0767},{"date":"2011-04-01","a":27.6863,"b":12.2308},{"date":"2011-05-01","a":12.3611,"b":7.0573},{"date":"2011-06-01","a":12.4269,"b":1.293},{"date":"2011-07-01","a":18.5765,"b":3.4815},{"date":"2011-08-01","a":9.1967,"b":14.4533},{"date":"2011-09-01","a":0.2613,"b":3.1618},{"date":"2011-10-01","a":3.1556,"b":9.6671},{"date":"2011-11-01","a":14.3516,"b":1.6119},{"date":"2011-12-01","a":12.755,"b":4.4683},{"date":"2012-01-01","a":20.1429,"b":5.7593},{"date":"2012-02-01","a":5.3441,"b":2.0097},{"date":"2012-03-01","a":6.2215,"b":15.8212},{"date":"2012-04-01","a":1.0995,"b":4.1461},{"date":"2012-05-01","a":11.7984,"b":5.9374},{"date":"2012-06-01","a":16.2198,"b":18.904},{"date":"2012-07-01","a":11.6513,"b":15.6244},{"date":"2012-08-01","a":11.3397,"b":6.1114}],"keys":{"value":["date","a","b"]},"type":"line","types":{"a":"line","b":"area"}},"opts":{"x":"date","y":null,"types":{"date":"Date","a":"numeric","b":"numeric"}},"axis":{"x":{"label":"date","type":"timeseries"},"y2":{"show":true}}},"evals":[],"jsHooks":[]}</script>

## Scatter Plot

``` r
mtcars %>%
  c3(x = 'mpg', 
     y = 'wt', 
     group = 'cyl') %>% 
  c3_scatter()
```

<div id="htmlwidget-8" style="width:672px;height:480px;" class="c3 html-widget"></div>
<script type="application/json" data-for="htmlwidget-8">{"x":{"data":{"json":[{"4":2.32,"6":2.62,"8":3.44,"4_x":22.8,"6_x":21,"8_x":18.7},{"4":3.19,"6":2.875,"8":3.57,"4_x":24.4,"6_x":21,"8_x":14.3},{"4":3.15,"6":3.215,"8":4.07,"4_x":22.8,"6_x":21.4,"8_x":16.4},{"4":2.2,"6":3.46,"8":3.73,"4_x":32.4,"6_x":18.1,"8_x":17.3},{"4":1.615,"6":3.44,"8":3.78,"4_x":30.4,"6_x":19.2,"8_x":15.2},{"4":1.835,"6":3.44,"8":5.25,"4_x":33.9,"6_x":17.8,"8_x":10.4},{"4":2.465,"6":2.77,"8":5.424,"4_x":21.5,"6_x":19.7,"8_x":10.4},{"4":1.935,"8":5.345,"4_x":27.3,"8_x":14.7},{"4":2.14,"8":3.52,"4_x":26,"8_x":15.5},{"4":1.513,"8":3.435,"4_x":30.4,"8_x":15.2},{"4":2.78,"8":3.84,"4_x":21.4,"8_x":13.3},{"8":3.845,"8_x":19.2},{"8":3.17,"8_x":15.8},{"8":3.57,"8_x":15}],"keys":{"value":["4","6","8","4_x","6_x","8_x"]},"xs":{"6":"6_x","4":"4_x","8":"8_x"},"type":"scatter"},"opts":{"x":"mpg","y":"wt","types":{"mpg":"numeric","cyl":"numeric","disp":"numeric","hp":"numeric","drat":"numeric","wt":"numeric","qsec":"numeric","vs":"numeric","am":"numeric","gear":"numeric","carb":"numeric"}},"axis":{"x":{"label":"mpg"},"y":{"label":"wt"}}},"evals":[],"jsHooks":[]}</script>

## Pie Charts

``` r
data.frame(India = 45,
           Bangladesh = 20,
           SriLanka = 10) %>% 
  c3() %>% 
  c3_pie()
```

<div id="htmlwidget-9" style="width:672px;height:480px;" class="c3 html-widget"></div>
<script type="application/json" data-for="htmlwidget-9">{"x":{"data":{"json":[{"India":45,"Bangladesh":20,"SriLanka":10}],"keys":{"value":["India","Bangladesh","SriLanka"]},"type":"pie"},"opts":{"x":null,"y":null,"types":{"India":"numeric","Bangladesh":"numeric","SriLanka":"numeric"}},"pie":{"expand":true,"label":{"show":true,"threshold":null,"format":null}}},"evals":[],"jsHooks":[]}</script>

## Donut Charts

``` r
data.frame(red = 82, green = 33, blue = 93) %>% 
  c3(colors = list(red = 'red',
                   green = 'green',
                   blue = 'blue')) %>% 
  c3_donut(title = '#d053ee')
```

<div id="htmlwidget-10" style="width:672px;height:480px;" class="c3 html-widget"></div>
<script type="application/json" data-for="htmlwidget-10">{"x":{"data":{"colors":{"red":"red","green":"green","blue":"blue"},"json":[{"red":82,"green":33,"blue":93}],"keys":{"value":["red","green","blue"]},"type":"donut"},"opts":{"x":null,"y":null,"types":{"red":"numeric","green":"numeric","blue":"numeric"}},"donut":{"expand":true,"title":"#d053ee","label":{"show":true,"threshold":null,"format":null}}},"evals":[],"jsHooks":[]}</script>

## Gauge Charts

``` r
data.frame(data = 80) %>% 
  c3() %>% 
  c3_gauge()
```

<div id="htmlwidget-11" style="width:672px;height:480px;" class="c3 html-widget"></div>
<script type="application/json" data-for="htmlwidget-11">{"x":{"data":{"json":[{"data":80}],"keys":{"value":["data"]},"type":"gauge"},"opts":{"x":null,"y":null,"types":{"data":"numeric"}},"gauge":{"label":null,"min":0,"max":100,"units":null,"width":null},"color":{"pattern":["#FF0000","#F97600","#F6C600","#60B044"],"threshold":{"unit":"value","max":100,"values":[30,60,90,100]}},"size":{"height":null}},"evals":[],"jsHooks":[]}</script>

## Grid Lines & Annotation

``` r
data %>%
  c3() %>%
  grid('y') %>%
  grid('x', 
       show = F, 
       lines = data.frame(value = c(3, 10), 
                          text= c('Line 1','Line 2')))
```

<div id="htmlwidget-12" style="width:672px;height:480px;" class="c3 html-widget"></div>
<script type="application/json" data-for="htmlwidget-12">{"x":{"data":{"json":[{"a":7.711,"b":0.9687,"c":3.4713,"d":12.656},{"a":2.8013,"b":6.1846,"c":8.2034,"d":12.205},{"a":1.8475,"b":10.0767,"c":16.5868,"d":20.0832},{"a":27.6863,"b":12.2308,"c":2.4936,"d":11.2891},{"a":12.3611,"b":7.0573,"c":10.6482,"d":12.2041},{"a":12.4269,"b":1.293,"c":3.7988,"d":6.1088},{"a":18.5765,"b":3.4815,"c":2.1802,"d":2.8879},{"a":9.1967,"b":14.4533,"c":8.3901,"d":3.1968},{"a":0.2613,"b":3.1618,"c":7.9922,"d":1.2813},{"a":3.1556,"b":9.6671,"c":10.4449,"d":12.0721},{"a":14.3516,"b":1.6119,"c":13.5387,"d":9.4406},{"a":12.755,"b":4.4683,"c":12.5018,"d":8.9714},{"a":20.1429,"b":5.7593,"c":9.9551,"d":5.182},{"a":5.3441,"b":2.0097,"c":15.0356,"d":0.8256},{"a":6.2215,"b":15.8212,"c":1.7341,"d":8.7247},{"a":1.0995,"b":4.1461,"c":9.2292,"d":9.2168},{"a":11.7984,"b":5.9374,"c":8.4761,"d":1.2355},{"a":16.2198,"b":18.904,"c":3.404,"d":12.0234},{"a":11.6513,"b":15.6244,"c":7.1839,"d":16.2478},{"a":11.3397,"b":6.1114,"c":13.8531,"d":5.6429}],"keys":{"value":["a","b","c","d"]}},"opts":{"x":null,"y":null,"types":{"a":"numeric","b":"numeric","date":"Date","c":"numeric","d":"numeric"}},"grid":{"y":{"show":true},"x":{"show":false,"lines":{"value":[3,10],"text":["Line 1","Line 2"]}}}},"evals":[],"jsHooks":[]}</script>

## Sub-chart

``` r
data %>%
  c3(x = 'date') %>%
  subchart()
```

<div id="htmlwidget-13" style="width:672px;height:480px;" class="c3 html-widget"></div>
<script type="application/json" data-for="htmlwidget-13">{"x":{"data":{"x":"date","json":[{"date":"2011-01-01","a":7.711,"b":0.9687,"c":3.4713,"d":12.656},{"date":"2011-02-01","a":2.8013,"b":6.1846,"c":8.2034,"d":12.205},{"date":"2011-03-01","a":1.8475,"b":10.0767,"c":16.5868,"d":20.0832},{"date":"2011-04-01","a":27.6863,"b":12.2308,"c":2.4936,"d":11.2891},{"date":"2011-05-01","a":12.3611,"b":7.0573,"c":10.6482,"d":12.2041},{"date":"2011-06-01","a":12.4269,"b":1.293,"c":3.7988,"d":6.1088},{"date":"2011-07-01","a":18.5765,"b":3.4815,"c":2.1802,"d":2.8879},{"date":"2011-08-01","a":9.1967,"b":14.4533,"c":8.3901,"d":3.1968},{"date":"2011-09-01","a":0.2613,"b":3.1618,"c":7.9922,"d":1.2813},{"date":"2011-10-01","a":3.1556,"b":9.6671,"c":10.4449,"d":12.0721},{"date":"2011-11-01","a":14.3516,"b":1.6119,"c":13.5387,"d":9.4406},{"date":"2011-12-01","a":12.755,"b":4.4683,"c":12.5018,"d":8.9714},{"date":"2012-01-01","a":20.1429,"b":5.7593,"c":9.9551,"d":5.182},{"date":"2012-02-01","a":5.3441,"b":2.0097,"c":15.0356,"d":0.8256},{"date":"2012-03-01","a":6.2215,"b":15.8212,"c":1.7341,"d":8.7247},{"date":"2012-04-01","a":1.0995,"b":4.1461,"c":9.2292,"d":9.2168},{"date":"2012-05-01","a":11.7984,"b":5.9374,"c":8.4761,"d":1.2355},{"date":"2012-06-01","a":16.2198,"b":18.904,"c":3.404,"d":12.0234},{"date":"2012-07-01","a":11.6513,"b":15.6244,"c":7.1839,"d":16.2478},{"date":"2012-08-01","a":11.3397,"b":6.1114,"c":13.8531,"d":5.6429}],"keys":{"value":["date","a","b","c","d"]}},"opts":{"x":"date","y":null,"types":{"a":"numeric","b":"numeric","date":"Date","c":"numeric","d":"numeric"}},"axis":{"x":{"label":"date","type":"timeseries"}},"subchart":{"show":true,"size":{"height":20}}},"evals":[],"jsHooks":[]}</script>

## Color Palette

Plot color palettes can be changed to either `RColorBrewer` or `viridis` palettes using either `RColorBrewer` (S3 method) or `c3_viridus`.

``` r
data.frame(sugar = 20, 
           fat = 45, 
           salt = 10, 
           vegetables = 60) %>% 
  c3() %>% 
  c3_pie() %>%
  RColorBrewer()
```

<div id="htmlwidget-14" style="width:672px;height:480px;" class="c3 html-widget"></div>
<script type="application/json" data-for="htmlwidget-14">{"x":{"data":{"json":[{"sugar":20,"fat":45,"salt":10,"vegetables":60}],"keys":{"value":["sugar","fat","salt","vegetables"]},"type":"pie"},"opts":{"x":null,"y":null,"types":{"sugar":"numeric","fat":"numeric","salt":"numeric","vegetables":"numeric"}},"pie":{"expand":true,"label":{"show":true,"threshold":null,"format":null}},"color":{"pattern":["#D7191C","#FDAE61","#ABDDA4","#2B83BA"]}},"evals":[],"jsHooks":[]}</script>

``` r
data.frame(sugar = 20, 
           fat = 45, 
           salt = 10, 
           vegetables = 60) %>% 
  c3() %>% 
  c3_pie() %>%
  c3_viridis()
```

<div id="htmlwidget-15" style="width:672px;height:480px;" class="c3 html-widget"></div>
<script type="application/json" data-for="htmlwidget-15">{"x":{"data":{"json":[{"sugar":20,"fat":45,"salt":10,"vegetables":60}],"keys":{"value":["sugar","fat","salt","vegetables"]},"type":"pie"},"opts":{"x":null,"y":null,"types":{"sugar":"numeric","fat":"numeric","salt":"numeric","vegetables":"numeric"}},"pie":{"expand":true,"label":{"show":true,"threshold":null,"format":null}},"color":{"pattern":["#440154","#31688E","#35B779","#FDE725"]}},"evals":[],"jsHooks":[]}</script>

## Point Size

``` r
data %>%
  c3(x = 'date') %>%
  point_options(r = 6, 
                expand.r = 2)
```

<div id="htmlwidget-16" style="width:672px;height:480px;" class="c3 html-widget"></div>
<script type="application/json" data-for="htmlwidget-16">{"x":{"data":{"x":"date","json":[{"date":"2011-01-01","a":7.711,"b":0.9687,"c":3.4713,"d":12.656},{"date":"2011-02-01","a":2.8013,"b":6.1846,"c":8.2034,"d":12.205},{"date":"2011-03-01","a":1.8475,"b":10.0767,"c":16.5868,"d":20.0832},{"date":"2011-04-01","a":27.6863,"b":12.2308,"c":2.4936,"d":11.2891},{"date":"2011-05-01","a":12.3611,"b":7.0573,"c":10.6482,"d":12.2041},{"date":"2011-06-01","a":12.4269,"b":1.293,"c":3.7988,"d":6.1088},{"date":"2011-07-01","a":18.5765,"b":3.4815,"c":2.1802,"d":2.8879},{"date":"2011-08-01","a":9.1967,"b":14.4533,"c":8.3901,"d":3.1968},{"date":"2011-09-01","a":0.2613,"b":3.1618,"c":7.9922,"d":1.2813},{"date":"2011-10-01","a":3.1556,"b":9.6671,"c":10.4449,"d":12.0721},{"date":"2011-11-01","a":14.3516,"b":1.6119,"c":13.5387,"d":9.4406},{"date":"2011-12-01","a":12.755,"b":4.4683,"c":12.5018,"d":8.9714},{"date":"2012-01-01","a":20.1429,"b":5.7593,"c":9.9551,"d":5.182},{"date":"2012-02-01","a":5.3441,"b":2.0097,"c":15.0356,"d":0.8256},{"date":"2012-03-01","a":6.2215,"b":15.8212,"c":1.7341,"d":8.7247},{"date":"2012-04-01","a":1.0995,"b":4.1461,"c":9.2292,"d":9.2168},{"date":"2012-05-01","a":11.7984,"b":5.9374,"c":8.4761,"d":1.2355},{"date":"2012-06-01","a":16.2198,"b":18.904,"c":3.404,"d":12.0234},{"date":"2012-07-01","a":11.6513,"b":15.6244,"c":7.1839,"d":16.2478},{"date":"2012-08-01","a":11.3397,"b":6.1114,"c":13.8531,"d":5.6429}],"keys":{"value":["date","a","b","c","d"]}},"opts":{"x":"date","y":null,"types":{"a":"numeric","b":"numeric","date":"Date","c":"numeric","d":"numeric"}},"axis":{"x":{"label":"date","type":"timeseries"}},"point":{"show":true,"r":6,"focus":{"expand":{"enabled":true,"r":12}},"select":{"r":24}}},"evals":[],"jsHooks":[]}</script>

## On Click

Onclick, onmouseover and onmouseout are all available via the `c3` function. To use wrap a js function as a character string to `htmlwidgets::JS()`. Please see the `C3.js` documentation and examples. The example below should be enough to get you started.

``` r
data %>% 
    c3(onclick = htmlwidgets::JS('function(d, element){console.log(d)}'))
```

<div id="htmlwidget-17" style="width:672px;height:480px;" class="c3 html-widget"></div>
<script type="application/json" data-for="htmlwidget-17">{"x":{"data":{"onclick":"function(d, element){console.log(d)}","json":[{"a":7.711,"b":0.9687,"c":3.4713,"d":12.656},{"a":2.8013,"b":6.1846,"c":8.2034,"d":12.205},{"a":1.8475,"b":10.0767,"c":16.5868,"d":20.0832},{"a":27.6863,"b":12.2308,"c":2.4936,"d":11.2891},{"a":12.3611,"b":7.0573,"c":10.6482,"d":12.2041},{"a":12.4269,"b":1.293,"c":3.7988,"d":6.1088},{"a":18.5765,"b":3.4815,"c":2.1802,"d":2.8879},{"a":9.1967,"b":14.4533,"c":8.3901,"d":3.1968},{"a":0.2613,"b":3.1618,"c":7.9922,"d":1.2813},{"a":3.1556,"b":9.6671,"c":10.4449,"d":12.0721},{"a":14.3516,"b":1.6119,"c":13.5387,"d":9.4406},{"a":12.755,"b":4.4683,"c":12.5018,"d":8.9714},{"a":20.1429,"b":5.7593,"c":9.9551,"d":5.182},{"a":5.3441,"b":2.0097,"c":15.0356,"d":0.8256},{"a":6.2215,"b":15.8212,"c":1.7341,"d":8.7247},{"a":1.0995,"b":4.1461,"c":9.2292,"d":9.2168},{"a":11.7984,"b":5.9374,"c":8.4761,"d":1.2355},{"a":16.2198,"b":18.904,"c":3.404,"d":12.0234},{"a":11.6513,"b":15.6244,"c":7.1839,"d":16.2478},{"a":11.3397,"b":6.1114,"c":13.8531,"d":5.6429}],"keys":{"value":["a","b","c","d"]}},"opts":{"x":null,"y":null,"types":{"a":"numeric","b":"numeric","date":"Date","c":"numeric","d":"numeric"}}},"evals":["data.onclick"],"jsHooks":[]}</script>

## Tooltips

C3 tooltips are readily modified with the use of javascript functions. For further detail see the `C3.js` documentation. Or for more advanced usage see the `C3.js` examples page.

``` r
library("htmlwidgets")
```

    ## Warning: package 'htmlwidgets' was built under R version 4.1.3

``` r
data %>%
  c3() %>%
  tooltip(format = list(title = JS("function (x) { return 'Data ' + x; }"),
                        name = JS('function (name, ratio, id, index) { return name; }'),
                        value = JS('function (value, ratio, id, index) { return ratio; }')))
```

<div id="htmlwidget-18" style="width:672px;height:480px;" class="c3 html-widget"></div>
<script type="application/json" data-for="htmlwidget-18">{"x":{"data":{"json":[{"a":7.711,"b":0.9687,"c":3.4713,"d":12.656},{"a":2.8013,"b":6.1846,"c":8.2034,"d":12.205},{"a":1.8475,"b":10.0767,"c":16.5868,"d":20.0832},{"a":27.6863,"b":12.2308,"c":2.4936,"d":11.2891},{"a":12.3611,"b":7.0573,"c":10.6482,"d":12.2041},{"a":12.4269,"b":1.293,"c":3.7988,"d":6.1088},{"a":18.5765,"b":3.4815,"c":2.1802,"d":2.8879},{"a":9.1967,"b":14.4533,"c":8.3901,"d":3.1968},{"a":0.2613,"b":3.1618,"c":7.9922,"d":1.2813},{"a":3.1556,"b":9.6671,"c":10.4449,"d":12.0721},{"a":14.3516,"b":1.6119,"c":13.5387,"d":9.4406},{"a":12.755,"b":4.4683,"c":12.5018,"d":8.9714},{"a":20.1429,"b":5.7593,"c":9.9551,"d":5.182},{"a":5.3441,"b":2.0097,"c":15.0356,"d":0.8256},{"a":6.2215,"b":15.8212,"c":1.7341,"d":8.7247},{"a":1.0995,"b":4.1461,"c":9.2292,"d":9.2168},{"a":11.7984,"b":5.9374,"c":8.4761,"d":1.2355},{"a":16.2198,"b":18.904,"c":3.404,"d":12.0234},{"a":11.6513,"b":15.6244,"c":7.1839,"d":16.2478},{"a":11.3397,"b":6.1114,"c":13.8531,"d":5.6429}],"keys":{"value":["a","b","c","d"]}},"opts":{"x":null,"y":null,"types":{"a":"numeric","b":"numeric","date":"Date","c":"numeric","d":"numeric"}},"tooltip":{"show":true,"grouped":true,"format":{"title":"function (x) { return 'Data ' + x; }","name":"function (name, ratio, id, index) { return name; }","value":"function (value, ratio, id, index) { return ratio; }"}}},"evals":["tooltip.format.title","tooltip.format.name","tooltip.format.value"],"jsHooks":[]}</script>
