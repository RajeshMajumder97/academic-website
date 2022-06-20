---
date: "2022-06-19T00:00:00Z"
external_link: ""
image:
#  caption: Photo by rawpixel on Unsplash
  focal_point: Smart
  
#slides: example
summary: The c3 package is a wrapper, or htmlwidget, for the C3 javascript charting library by Masayuki Tanaka. 
categories: ["R"]
tags:
- Blogs
title: C3

output:
  blogdown::html_page:
    toc: true
      
---

<script src="/rmarkdown-libs/htmlwidgets/htmlwidgets.js"></script>
<script src="/rmarkdown-libs/d3/d3.min.js"></script>
<link href="/rmarkdown-libs/c3/c3.min.css" rel="stylesheet" />
<script src="/rmarkdown-libs/c3/c3.min.js"></script>
<script src="/rmarkdown-libs/c3-binding/c3.js"></script>
<script src="/rmarkdown-libs/htmlwidgets/htmlwidgets.js"></script>
<script src="/rmarkdown-libs/d3/d3.min.js"></script>
<link href="/rmarkdown-libs/c3/c3.min.css" rel="stylesheet" />
<script src="/rmarkdown-libs/c3/c3.min.js"></script>
<script src="/rmarkdown-libs/c3-binding/c3.js"></script>
<script src="/rmarkdown-libs/htmlwidgets/htmlwidgets.js"></script>
<script src="/rmarkdown-libs/d3/d3.min.js"></script>
<link href="/rmarkdown-libs/c3/c3.min.css" rel="stylesheet" />
<script src="/rmarkdown-libs/c3/c3.min.js"></script>
<script src="/rmarkdown-libs/c3-binding/c3.js"></script>
<script src="/rmarkdown-libs/htmlwidgets/htmlwidgets.js"></script>
<script src="/rmarkdown-libs/d3/d3.min.js"></script>
<link href="/rmarkdown-libs/c3/c3.min.css" rel="stylesheet" />
<script src="/rmarkdown-libs/c3/c3.min.js"></script>
<script src="/rmarkdown-libs/c3-binding/c3.js"></script>
<script src="/rmarkdown-libs/htmlwidgets/htmlwidgets.js"></script>
<script src="/rmarkdown-libs/d3/d3.min.js"></script>
<link href="/rmarkdown-libs/c3/c3.min.css" rel="stylesheet" />
<script src="/rmarkdown-libs/c3/c3.min.js"></script>
<script src="/rmarkdown-libs/c3-binding/c3.js"></script>
<script src="/rmarkdown-libs/htmlwidgets/htmlwidgets.js"></script>
<script src="/rmarkdown-libs/d3/d3.min.js"></script>
<link href="/rmarkdown-libs/c3/c3.min.css" rel="stylesheet" />
<script src="/rmarkdown-libs/c3/c3.min.js"></script>
<script src="/rmarkdown-libs/c3-binding/c3.js"></script>
<script src="/rmarkdown-libs/htmlwidgets/htmlwidgets.js"></script>
<script src="/rmarkdown-libs/d3/d3.min.js"></script>
<link href="/rmarkdown-libs/c3/c3.min.css" rel="stylesheet" />
<script src="/rmarkdown-libs/c3/c3.min.js"></script>
<script src="/rmarkdown-libs/c3-binding/c3.js"></script>
<script src="/rmarkdown-libs/htmlwidgets/htmlwidgets.js"></script>
<script src="/rmarkdown-libs/d3/d3.min.js"></script>
<link href="/rmarkdown-libs/c3/c3.min.css" rel="stylesheet" />
<script src="/rmarkdown-libs/c3/c3.min.js"></script>
<script src="/rmarkdown-libs/c3-binding/c3.js"></script>
<script src="/rmarkdown-libs/htmlwidgets/htmlwidgets.js"></script>
<script src="/rmarkdown-libs/d3/d3.min.js"></script>
<link href="/rmarkdown-libs/c3/c3.min.css" rel="stylesheet" />
<script src="/rmarkdown-libs/c3/c3.min.js"></script>
<script src="/rmarkdown-libs/c3-binding/c3.js"></script>
<script src="/rmarkdown-libs/htmlwidgets/htmlwidgets.js"></script>
<script src="/rmarkdown-libs/d3/d3.min.js"></script>
<link href="/rmarkdown-libs/c3/c3.min.css" rel="stylesheet" />
<script src="/rmarkdown-libs/c3/c3.min.js"></script>
<script src="/rmarkdown-libs/c3-binding/c3.js"></script>
<script src="/rmarkdown-libs/htmlwidgets/htmlwidgets.js"></script>
<script src="/rmarkdown-libs/d3/d3.min.js"></script>
<link href="/rmarkdown-libs/c3/c3.min.css" rel="stylesheet" />
<script src="/rmarkdown-libs/c3/c3.min.js"></script>
<script src="/rmarkdown-libs/c3-binding/c3.js"></script>
<script src="/rmarkdown-libs/htmlwidgets/htmlwidgets.js"></script>
<script src="/rmarkdown-libs/d3/d3.min.js"></script>
<link href="/rmarkdown-libs/c3/c3.min.css" rel="stylesheet" />
<script src="/rmarkdown-libs/c3/c3.min.js"></script>
<script src="/rmarkdown-libs/c3-binding/c3.js"></script>
<script src="/rmarkdown-libs/htmlwidgets/htmlwidgets.js"></script>
<script src="/rmarkdown-libs/d3/d3.min.js"></script>
<link href="/rmarkdown-libs/c3/c3.min.css" rel="stylesheet" />
<script src="/rmarkdown-libs/c3/c3.min.js"></script>
<script src="/rmarkdown-libs/c3-binding/c3.js"></script>
<script src="/rmarkdown-libs/htmlwidgets/htmlwidgets.js"></script>
<script src="/rmarkdown-libs/d3/d3.min.js"></script>
<link href="/rmarkdown-libs/c3/c3.min.css" rel="stylesheet" />
<script src="/rmarkdown-libs/c3/c3.min.js"></script>
<script src="/rmarkdown-libs/c3-binding/c3.js"></script>
<script src="/rmarkdown-libs/htmlwidgets/htmlwidgets.js"></script>
<script src="/rmarkdown-libs/d3/d3.min.js"></script>
<link href="/rmarkdown-libs/c3/c3.min.css" rel="stylesheet" />
<script src="/rmarkdown-libs/c3/c3.min.js"></script>
<script src="/rmarkdown-libs/c3-binding/c3.js"></script>
<script src="/rmarkdown-libs/htmlwidgets/htmlwidgets.js"></script>
<script src="/rmarkdown-libs/d3/d3.min.js"></script>
<link href="/rmarkdown-libs/c3/c3.min.css" rel="stylesheet" />
<script src="/rmarkdown-libs/c3/c3.min.js"></script>
<script src="/rmarkdown-libs/c3-binding/c3.js"></script>
<script src="/rmarkdown-libs/htmlwidgets/htmlwidgets.js"></script>
<script src="/rmarkdown-libs/d3/d3.min.js"></script>
<link href="/rmarkdown-libs/c3/c3.min.css" rel="stylesheet" />
<script src="/rmarkdown-libs/c3/c3.min.js"></script>
<script src="/rmarkdown-libs/c3-binding/c3.js"></script>
<script src="/rmarkdown-libs/htmlwidgets/htmlwidgets.js"></script>
<script src="/rmarkdown-libs/d3/d3.min.js"></script>
<link href="/rmarkdown-libs/c3/c3.min.css" rel="stylesheet" />
<script src="/rmarkdown-libs/c3/c3.min.js"></script>
<script src="/rmarkdown-libs/c3-binding/c3.js"></script>

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
<script type="application/json" data-for="htmlwidget-1">{"x":{"data":{"json":[{"a":4.858,"b":10.4599},{"a":1.5774,"b":9.315},{"a":0.7599,"b":9.0915},{"a":1.2935,"b":1.8001},{"a":11.6133,"b":15.2389},{"a":9.7968,"b":0.4072},{"a":7.1887,"b":7.0839},{"a":0.6286,"b":9.6595},{"a":1.1505,"b":5.669},{"a":4.8779,"b":5.0453},{"a":3.4708,"b":6.0874},{"a":13.3892,"b":0.7775},{"a":5.103,"b":5.3326},{"a":11.3793,"b":16.2103},{"a":13.9982,"b":10.6907},{"a":7.1474,"b":0.7392},{"a":5.7962,"b":4.3492},{"a":17.1896,"b":7.3961},{"a":1.1301,"b":11.9677},{"a":5.9111,"b":7.0234}],"keys":{"value":["a","b"]}},"opts":{"x":null,"y":null,"types":{"a":"numeric","b":"numeric","date":"Date"}}},"evals":[],"jsHooks":[]}</script>

### Piping

The package also imports the magrittr piping function `(%>%)` to simplify syntax.

``` r
data%>%c3()
```

<div id="htmlwidget-2" style="width:672px;height:480px;" class="c3 html-widget"></div>
<script type="application/json" data-for="htmlwidget-2">{"x":{"data":{"json":[{"a":4.858,"b":10.4599},{"a":1.5774,"b":9.315},{"a":0.7599,"b":9.0915},{"a":1.2935,"b":1.8001},{"a":11.6133,"b":15.2389},{"a":9.7968,"b":0.4072},{"a":7.1887,"b":7.0839},{"a":0.6286,"b":9.6595},{"a":1.1505,"b":5.669},{"a":4.8779,"b":5.0453},{"a":3.4708,"b":6.0874},{"a":13.3892,"b":0.7775},{"a":5.103,"b":5.3326},{"a":11.3793,"b":16.2103},{"a":13.9982,"b":10.6907},{"a":7.1474,"b":0.7392},{"a":5.7962,"b":4.3492},{"a":17.1896,"b":7.3961},{"a":1.1301,"b":11.9677},{"a":5.9111,"b":7.0234}],"keys":{"value":["a","b"]}},"opts":{"x":null,"y":null,"types":{"a":"numeric","b":"numeric","date":"Date"}}},"evals":[],"jsHooks":[]}</script>

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
<script type="application/json" data-for="htmlwidget-3">{"x":{"data":{"json":[{"a":4.858,"b":10.4599},{"a":1.5774,"b":9.315},{"a":0.7599,"b":9.0915},{"a":1.2935,"b":1.8001},{"a":11.6133,"b":15.2389},{"a":9.7968,"b":0.4072},{"a":7.1887,"b":7.0839},{"a":0.6286,"b":9.6595},{"a":1.1505,"b":5.669},{"a":4.8779,"b":5.0453},{"a":3.4708,"b":6.0874},{"a":13.3892,"b":0.7775},{"a":5.103,"b":5.3326},{"a":11.3793,"b":16.2103},{"a":13.9982,"b":10.6907},{"a":7.1474,"b":0.7392},{"a":5.7962,"b":4.3492},{"a":17.1896,"b":7.3961},{"a":1.1301,"b":11.9677},{"a":5.9111,"b":7.0234}],"keys":{"value":["a","b"]},"type":"spline"},"opts":{"x":null,"y":null,"types":{"a":"numeric","b":"numeric","date":"Date"}}},"evals":[],"jsHooks":[]}</script>

### Step

``` r
data %>%
  c3(x = 'date') %>%
  c3_line('area-step')
```

<div id="htmlwidget-4" style="width:672px;height:480px;" class="c3 html-widget"></div>
<script type="application/json" data-for="htmlwidget-4">{"x":{"data":{"x":"date","json":[{"date":"2011-01-01","a":4.858,"b":10.4599},{"date":"2011-02-01","a":1.5774,"b":9.315},{"date":"2011-03-01","a":0.7599,"b":9.0915},{"date":"2011-04-01","a":1.2935,"b":1.8001},{"date":"2011-05-01","a":11.6133,"b":15.2389},{"date":"2011-06-01","a":9.7968,"b":0.4072},{"date":"2011-07-01","a":7.1887,"b":7.0839},{"date":"2011-08-01","a":0.6286,"b":9.6595},{"date":"2011-09-01","a":1.1505,"b":5.669},{"date":"2011-10-01","a":4.8779,"b":5.0453},{"date":"2011-11-01","a":3.4708,"b":6.0874},{"date":"2011-12-01","a":13.3892,"b":0.7775},{"date":"2012-01-01","a":5.103,"b":5.3326},{"date":"2012-02-01","a":11.3793,"b":16.2103},{"date":"2012-03-01","a":13.9982,"b":10.6907},{"date":"2012-04-01","a":7.1474,"b":0.7392},{"date":"2012-05-01","a":5.7962,"b":4.3492},{"date":"2012-06-01","a":17.1896,"b":7.3961},{"date":"2012-07-01","a":1.1301,"b":11.9677},{"date":"2012-08-01","a":5.9111,"b":7.0234}],"keys":{"value":["date","a","b"]},"type":"area-step"},"opts":{"x":"date","y":null,"types":{"a":"numeric","b":"numeric","date":"Date"}},"axis":{"x":{"label":"date","type":"timeseries"}}},"evals":[],"jsHooks":[]}</script>

## Bar Plots

``` r
data[1:10, ] %>%
  c3() %>%
  c3_bar(stacked = TRUE, 
         rotate = TRUE)
```

<div id="htmlwidget-5" style="width:672px;height:480px;" class="c3 html-widget"></div>
<script type="application/json" data-for="htmlwidget-5">{"x":{"data":{"json":[{"a":4.858,"b":10.4599},{"a":1.5774,"b":9.315},{"a":0.7599,"b":9.0915},{"a":1.2935,"b":1.8001},{"a":11.6133,"b":15.2389},{"a":9.7968,"b":0.4072},{"a":7.1887,"b":7.0839},{"a":0.6286,"b":9.6595},{"a":1.1505,"b":5.669},{"a":4.8779,"b":5.0453}],"keys":{"value":["a","b"]},"type":"bar","groups":{"value":["a","b"]}},"opts":{"x":null,"y":null,"types":{"a":"numeric","b":"numeric","date":"Date"}},"axis":{"x":{"type":"category"},"rotated":true},"bar":{"zerobased":true,"width":{"ratio":0.6}}},"evals":[],"jsHooks":[]}</script>

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
<script type="application/json" data-for="htmlwidget-6">{"x":{"data":{"json":[{"a":4.858,"b":10.4599,"c":1.4023,"d":14.1289},{"a":1.5774,"b":9.315,"c":0.2553,"d":17.6621},{"a":0.7599,"b":9.0915,"c":8.3665,"d":18.92},{"a":1.2935,"b":1.8001,"c":18.6624,"d":0.689},{"a":11.6133,"b":15.2389,"c":20.6581,"d":12.0983},{"a":9.7968,"b":0.4072,"c":2.4612,"d":14.4661},{"a":7.1887,"b":7.0839,"c":0.787,"d":12.1548},{"a":0.6286,"b":9.6595,"c":8.5938,"d":17.153},{"a":1.1505,"b":5.669,"c":12.324,"d":0.9452},{"a":4.8779,"b":5.0453,"c":2.6081,"d":11.4216},{"a":3.4708,"b":6.0874,"c":12.8448,"d":13.2329},{"a":13.3892,"b":0.7775,"c":9.1635,"d":4.2314},{"a":5.103,"b":5.3326,"c":7.3258,"d":2.4164},{"a":11.3793,"b":16.2103,"c":9.7296,"d":3.9985},{"a":13.9982,"b":10.6907,"c":2.0652,"d":13.8608},{"a":7.1474,"b":0.7392,"c":5.0592,"d":10.9323},{"a":5.7962,"b":4.3492,"c":11.2524,"d":1.3589},{"a":17.1896,"b":7.3961,"c":1.3359,"d":6.3413},{"a":1.1301,"b":11.9677,"c":25.7613,"d":1.9029},{"a":5.9111,"b":7.0234,"c":1.3575,"d":13.7361}],"keys":{"value":["a","b","c","d"]},"type":"bar","types":{"a":"area","c":"spline"},"groups":["b","d"]},"opts":{"x":null,"y":null,"types":{"a":"numeric","b":"numeric","date":"Date","c":"numeric","d":"numeric"}}},"evals":[],"jsHooks":[]}</script>

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
<script type="application/json" data-for="htmlwidget-7">{"x":{"data":{"axes":{"a":"y","b":"y2"},"x":"date","json":[{"date":"2011-01-01","a":4.858,"b":10.4599},{"date":"2011-02-01","a":1.5774,"b":9.315},{"date":"2011-03-01","a":0.7599,"b":9.0915},{"date":"2011-04-01","a":1.2935,"b":1.8001},{"date":"2011-05-01","a":11.6133,"b":15.2389},{"date":"2011-06-01","a":9.7968,"b":0.4072},{"date":"2011-07-01","a":7.1887,"b":7.0839},{"date":"2011-08-01","a":0.6286,"b":9.6595},{"date":"2011-09-01","a":1.1505,"b":5.669},{"date":"2011-10-01","a":4.8779,"b":5.0453},{"date":"2011-11-01","a":3.4708,"b":6.0874},{"date":"2011-12-01","a":13.3892,"b":0.7775},{"date":"2012-01-01","a":5.103,"b":5.3326},{"date":"2012-02-01","a":11.3793,"b":16.2103},{"date":"2012-03-01","a":13.9982,"b":10.6907},{"date":"2012-04-01","a":7.1474,"b":0.7392},{"date":"2012-05-01","a":5.7962,"b":4.3492},{"date":"2012-06-01","a":17.1896,"b":7.3961},{"date":"2012-07-01","a":1.1301,"b":11.9677},{"date":"2012-08-01","a":5.9111,"b":7.0234}],"keys":{"value":["date","a","b"]},"type":"line","types":{"a":"line","b":"area"}},"opts":{"x":"date","y":null,"types":{"date":"Date","a":"numeric","b":"numeric"}},"axis":{"x":{"label":"date","type":"timeseries"},"y2":{"show":true}}},"evals":[],"jsHooks":[]}</script>

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
<script type="application/json" data-for="htmlwidget-12">{"x":{"data":{"json":[{"a":4.858,"b":10.4599,"c":1.4023,"d":14.1289},{"a":1.5774,"b":9.315,"c":0.2553,"d":17.6621},{"a":0.7599,"b":9.0915,"c":8.3665,"d":18.92},{"a":1.2935,"b":1.8001,"c":18.6624,"d":0.689},{"a":11.6133,"b":15.2389,"c":20.6581,"d":12.0983},{"a":9.7968,"b":0.4072,"c":2.4612,"d":14.4661},{"a":7.1887,"b":7.0839,"c":0.787,"d":12.1548},{"a":0.6286,"b":9.6595,"c":8.5938,"d":17.153},{"a":1.1505,"b":5.669,"c":12.324,"d":0.9452},{"a":4.8779,"b":5.0453,"c":2.6081,"d":11.4216},{"a":3.4708,"b":6.0874,"c":12.8448,"d":13.2329},{"a":13.3892,"b":0.7775,"c":9.1635,"d":4.2314},{"a":5.103,"b":5.3326,"c":7.3258,"d":2.4164},{"a":11.3793,"b":16.2103,"c":9.7296,"d":3.9985},{"a":13.9982,"b":10.6907,"c":2.0652,"d":13.8608},{"a":7.1474,"b":0.7392,"c":5.0592,"d":10.9323},{"a":5.7962,"b":4.3492,"c":11.2524,"d":1.3589},{"a":17.1896,"b":7.3961,"c":1.3359,"d":6.3413},{"a":1.1301,"b":11.9677,"c":25.7613,"d":1.9029},{"a":5.9111,"b":7.0234,"c":1.3575,"d":13.7361}],"keys":{"value":["a","b","c","d"]}},"opts":{"x":null,"y":null,"types":{"a":"numeric","b":"numeric","date":"Date","c":"numeric","d":"numeric"}},"grid":{"y":{"show":true},"x":{"show":false,"lines":{"value":[3,10],"text":["Line 1","Line 2"]}}}},"evals":[],"jsHooks":[]}</script>

## Sub-chart

``` r
data %>%
  c3(x = 'date') %>%
  subchart()
```

<div id="htmlwidget-13" style="width:672px;height:480px;" class="c3 html-widget"></div>
<script type="application/json" data-for="htmlwidget-13">{"x":{"data":{"x":"date","json":[{"date":"2011-01-01","a":4.858,"b":10.4599,"c":1.4023,"d":14.1289},{"date":"2011-02-01","a":1.5774,"b":9.315,"c":0.2553,"d":17.6621},{"date":"2011-03-01","a":0.7599,"b":9.0915,"c":8.3665,"d":18.92},{"date":"2011-04-01","a":1.2935,"b":1.8001,"c":18.6624,"d":0.689},{"date":"2011-05-01","a":11.6133,"b":15.2389,"c":20.6581,"d":12.0983},{"date":"2011-06-01","a":9.7968,"b":0.4072,"c":2.4612,"d":14.4661},{"date":"2011-07-01","a":7.1887,"b":7.0839,"c":0.787,"d":12.1548},{"date":"2011-08-01","a":0.6286,"b":9.6595,"c":8.5938,"d":17.153},{"date":"2011-09-01","a":1.1505,"b":5.669,"c":12.324,"d":0.9452},{"date":"2011-10-01","a":4.8779,"b":5.0453,"c":2.6081,"d":11.4216},{"date":"2011-11-01","a":3.4708,"b":6.0874,"c":12.8448,"d":13.2329},{"date":"2011-12-01","a":13.3892,"b":0.7775,"c":9.1635,"d":4.2314},{"date":"2012-01-01","a":5.103,"b":5.3326,"c":7.3258,"d":2.4164},{"date":"2012-02-01","a":11.3793,"b":16.2103,"c":9.7296,"d":3.9985},{"date":"2012-03-01","a":13.9982,"b":10.6907,"c":2.0652,"d":13.8608},{"date":"2012-04-01","a":7.1474,"b":0.7392,"c":5.0592,"d":10.9323},{"date":"2012-05-01","a":5.7962,"b":4.3492,"c":11.2524,"d":1.3589},{"date":"2012-06-01","a":17.1896,"b":7.3961,"c":1.3359,"d":6.3413},{"date":"2012-07-01","a":1.1301,"b":11.9677,"c":25.7613,"d":1.9029},{"date":"2012-08-01","a":5.9111,"b":7.0234,"c":1.3575,"d":13.7361}],"keys":{"value":["date","a","b","c","d"]}},"opts":{"x":"date","y":null,"types":{"a":"numeric","b":"numeric","date":"Date","c":"numeric","d":"numeric"}},"axis":{"x":{"label":"date","type":"timeseries"}},"subchart":{"show":true,"size":{"height":20}}},"evals":[],"jsHooks":[]}</script>

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
<script type="application/json" data-for="htmlwidget-16">{"x":{"data":{"x":"date","json":[{"date":"2011-01-01","a":4.858,"b":10.4599,"c":1.4023,"d":14.1289},{"date":"2011-02-01","a":1.5774,"b":9.315,"c":0.2553,"d":17.6621},{"date":"2011-03-01","a":0.7599,"b":9.0915,"c":8.3665,"d":18.92},{"date":"2011-04-01","a":1.2935,"b":1.8001,"c":18.6624,"d":0.689},{"date":"2011-05-01","a":11.6133,"b":15.2389,"c":20.6581,"d":12.0983},{"date":"2011-06-01","a":9.7968,"b":0.4072,"c":2.4612,"d":14.4661},{"date":"2011-07-01","a":7.1887,"b":7.0839,"c":0.787,"d":12.1548},{"date":"2011-08-01","a":0.6286,"b":9.6595,"c":8.5938,"d":17.153},{"date":"2011-09-01","a":1.1505,"b":5.669,"c":12.324,"d":0.9452},{"date":"2011-10-01","a":4.8779,"b":5.0453,"c":2.6081,"d":11.4216},{"date":"2011-11-01","a":3.4708,"b":6.0874,"c":12.8448,"d":13.2329},{"date":"2011-12-01","a":13.3892,"b":0.7775,"c":9.1635,"d":4.2314},{"date":"2012-01-01","a":5.103,"b":5.3326,"c":7.3258,"d":2.4164},{"date":"2012-02-01","a":11.3793,"b":16.2103,"c":9.7296,"d":3.9985},{"date":"2012-03-01","a":13.9982,"b":10.6907,"c":2.0652,"d":13.8608},{"date":"2012-04-01","a":7.1474,"b":0.7392,"c":5.0592,"d":10.9323},{"date":"2012-05-01","a":5.7962,"b":4.3492,"c":11.2524,"d":1.3589},{"date":"2012-06-01","a":17.1896,"b":7.3961,"c":1.3359,"d":6.3413},{"date":"2012-07-01","a":1.1301,"b":11.9677,"c":25.7613,"d":1.9029},{"date":"2012-08-01","a":5.9111,"b":7.0234,"c":1.3575,"d":13.7361}],"keys":{"value":["date","a","b","c","d"]}},"opts":{"x":"date","y":null,"types":{"a":"numeric","b":"numeric","date":"Date","c":"numeric","d":"numeric"}},"axis":{"x":{"label":"date","type":"timeseries"}},"point":{"show":true,"r":6,"focus":{"expand":{"enabled":true,"r":12}},"select":{"r":24}}},"evals":[],"jsHooks":[]}</script>

## On Click

Onclick, onmouseover and onmouseout are all available via the `c3` function. To use wrap a js function as a character string to `htmlwidgets::JS()`. Please see the `C3.js` documentation and examples. The example below should be enough to get you started.

``` r
data %>% 
    c3(onclick = htmlwidgets::JS('function(d, element){console.log(d)}'))
```

<div id="htmlwidget-17" style="width:672px;height:480px;" class="c3 html-widget"></div>
<script type="application/json" data-for="htmlwidget-17">{"x":{"data":{"onclick":"function(d, element){console.log(d)}","json":[{"a":4.858,"b":10.4599,"c":1.4023,"d":14.1289},{"a":1.5774,"b":9.315,"c":0.2553,"d":17.6621},{"a":0.7599,"b":9.0915,"c":8.3665,"d":18.92},{"a":1.2935,"b":1.8001,"c":18.6624,"d":0.689},{"a":11.6133,"b":15.2389,"c":20.6581,"d":12.0983},{"a":9.7968,"b":0.4072,"c":2.4612,"d":14.4661},{"a":7.1887,"b":7.0839,"c":0.787,"d":12.1548},{"a":0.6286,"b":9.6595,"c":8.5938,"d":17.153},{"a":1.1505,"b":5.669,"c":12.324,"d":0.9452},{"a":4.8779,"b":5.0453,"c":2.6081,"d":11.4216},{"a":3.4708,"b":6.0874,"c":12.8448,"d":13.2329},{"a":13.3892,"b":0.7775,"c":9.1635,"d":4.2314},{"a":5.103,"b":5.3326,"c":7.3258,"d":2.4164},{"a":11.3793,"b":16.2103,"c":9.7296,"d":3.9985},{"a":13.9982,"b":10.6907,"c":2.0652,"d":13.8608},{"a":7.1474,"b":0.7392,"c":5.0592,"d":10.9323},{"a":5.7962,"b":4.3492,"c":11.2524,"d":1.3589},{"a":17.1896,"b":7.3961,"c":1.3359,"d":6.3413},{"a":1.1301,"b":11.9677,"c":25.7613,"d":1.9029},{"a":5.9111,"b":7.0234,"c":1.3575,"d":13.7361}],"keys":{"value":["a","b","c","d"]}},"opts":{"x":null,"y":null,"types":{"a":"numeric","b":"numeric","date":"Date","c":"numeric","d":"numeric"}}},"evals":["data.onclick"],"jsHooks":[]}</script>

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
<script type="application/json" data-for="htmlwidget-18">{"x":{"data":{"json":[{"a":4.858,"b":10.4599,"c":1.4023,"d":14.1289},{"a":1.5774,"b":9.315,"c":0.2553,"d":17.6621},{"a":0.7599,"b":9.0915,"c":8.3665,"d":18.92},{"a":1.2935,"b":1.8001,"c":18.6624,"d":0.689},{"a":11.6133,"b":15.2389,"c":20.6581,"d":12.0983},{"a":9.7968,"b":0.4072,"c":2.4612,"d":14.4661},{"a":7.1887,"b":7.0839,"c":0.787,"d":12.1548},{"a":0.6286,"b":9.6595,"c":8.5938,"d":17.153},{"a":1.1505,"b":5.669,"c":12.324,"d":0.9452},{"a":4.8779,"b":5.0453,"c":2.6081,"d":11.4216},{"a":3.4708,"b":6.0874,"c":12.8448,"d":13.2329},{"a":13.3892,"b":0.7775,"c":9.1635,"d":4.2314},{"a":5.103,"b":5.3326,"c":7.3258,"d":2.4164},{"a":11.3793,"b":16.2103,"c":9.7296,"d":3.9985},{"a":13.9982,"b":10.6907,"c":2.0652,"d":13.8608},{"a":7.1474,"b":0.7392,"c":5.0592,"d":10.9323},{"a":5.7962,"b":4.3492,"c":11.2524,"d":1.3589},{"a":17.1896,"b":7.3961,"c":1.3359,"d":6.3413},{"a":1.1301,"b":11.9677,"c":25.7613,"d":1.9029},{"a":5.9111,"b":7.0234,"c":1.3575,"d":13.7361}],"keys":{"value":["a","b","c","d"]}},"opts":{"x":null,"y":null,"types":{"a":"numeric","b":"numeric","date":"Date","c":"numeric","d":"numeric"}},"tooltip":{"show":true,"grouped":true,"format":{"title":"function (x) { return 'Data ' + x; }","name":"function (name, ratio, id, index) { return name; }","value":"function (value, ratio, id, index) { return ratio; }"}}},"evals":["tooltip.format.title","tooltip.format.name","tooltip.format.value"],"jsHooks":[]}</script>
