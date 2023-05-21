---
title: "A third post"
weight: 3
subtitle: ""
excerpt: "This is an excerpt for post 3"
date: 2021-01-03
draft: false
---

<script src="{{< blogdown/postref >}}index_files/htmlwidgets/htmlwidgets.js"></script>
<script src="{{< blogdown/postref >}}index_files/echarts4r/echarts-en.min.js"></script>
<script src="{{< blogdown/postref >}}index_files/echarts4r/ecStat.min.js"></script>
<script src="{{< blogdown/postref >}}index_files/echarts4r/dataTool.min.js"></script>
<script src="{{< blogdown/postref >}}index_files/echarts4r-binding/echarts4r.js"></script>

``` r
library(echarts4r)
library(palmerpenguins)
library(dplyr)
```

    ## 
    ## Attaching package: 'dplyr'

    ## The following objects are masked from 'package:stats':
    ## 
    ##     filter, lag

    ## The following objects are masked from 'package:base':
    ## 
    ##     intersect, setdiff, setequal, union

``` r
palmerpenguins::penguins %>% 
    group_by(species) %>% 
    summarise(avg_body_mass = mean(body_mass_g, na.rm = TRUE)) %>% 
    e_charts(x = species) %>% 
    e_bar(serie = avg_body_mass, name = "Avg. Body Mass") %>% 
    e_tooltip(formatter = e_tooltip_item_formatter()) %>% 
    e_axis_labels(x = "Species", y = "Body Mass (g)")
```

<div class="echarts4r html-widget html-fill-item-overflow-hidden html-fill-item" id="htmlwidget-1" style="width:100%;height:500px;"></div>
<script type="application/json" data-for="htmlwidget-1">{"x":{"theme":"","tl":false,"draw":true,"renderer":"canvas","events":[],"buttons":[],"opts":{"yAxis":[{"show":true,"name":"Body Mass (g)"}],"xAxis":[{"data":["Adelie","Chinstrap","Gentoo"],"type":"category","boundaryGap":true,"name":"Species"}],"legend":{"data":["Avg. Body Mass"]},"series":[{"data":[{"value":["Adelie","3700.662"]},{"value":["Chinstrap","3733.088"]},{"value":["Gentoo","5076.016"]}],"name":"Avg. Body Mass","type":"bar","yAxisIndex":0,"xAxisIndex":0,"coordinateSystem":"cartesian2d"}],"tooltip":{"trigger":"item","formatter":"function(params, ticket, callback) {\n        var fmt = new Intl.NumberFormat('en', {\"style\":\"decimal\",\"minimumFractionDigits\":0,\"maximumFractionDigits\":0,\"currency\":\"USD\"});\n        var idx = 0;\n        if (params.name == params.value[0]) {\n            idx = 1;\n        }\n        return params.value[0] + '<br>' +\n               params.marker + ' ' +\n               params.seriesName + ': ' + fmt.format(parseFloat(params.value[idx]));\n    }"}},"dispose":true},"evals":["opts.tooltip.formatter"],"jsHooks":[]}</script>

## are you still here?

### does this work?

------------------------------------------------------------------------

## final stretch!
