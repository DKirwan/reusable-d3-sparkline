# D3 Sparkline Chart

![Reusable D3.js Sparkline chart](https://raw.githubusercontent.com/DKirwan/reusable-d3-sparkline/develop/thumbnail.png)

This chart was built with Mike Bostock's [reusable D3.js charts best practice](http://bost.ocks.org/mike/chart/) in mind.

## What is a sparkline chart?

[From Wikipedia](https://en.wikipedia.org/wiki/Sparkline) A sparkline is a very small line chart, typically drawn without axes or coordinates. It presents the general shape of the variation (typically over time) in some measurement, such as temperature or stock market price, in a simple and highly condensed way. Sparklines are small enough to be embedded in text, or several sparklines may be grouped together as elements of a small multiple. Whereas the typical chart is designed to show as much data as possible, and is set off from the flow of text, sparklines are intended to be succinct, memorable, and located where they are discussed

## Configuration

|Property        | Usage           | Default  | Required |
|:------------- |:-------------|:-----:|:-----:|
| width      | width in pixels | 175 | no |
| height      | height in pixels |   56 | no |
| dataSource | file path, relative to the sparkline.js file | none | yes |
| dataSourceType | type of data source. Must be one of CSV, TSV or JSON | none | yes |
| selector | DOM selector to attach the chart to | body | no |
| gradientColors | Array of colours for the gradient, from max to min | [green, orange, red] | no |

## Usage

1: Include the sparkline.js code
`<script src="path/to/sparkline.js"></script>`

2: Format the data so it has a `date` and `count` property
As long as `new Date()` can parse the date string it's ok.

3: Then configure the chart and render it
```javascript
var chart1 = sparkline()
              .width(155)
              .height(50)
              .gradientColors(['lightblue', 'steelblue', 'blue', navy]) // top -> bottom
              .dataSource('ry4c.csv') // relative to sparkline.js
              .dataSourceType('CSV')
              .selector('#chart-one');
var chart2 = sparkline()
              .width(155)
              .height(50)
              .dataSource('ezj.tsv') // relative to sparkline.js
              .dataSourceType('TSV')
              .selector('#chart-two');
chart1();  // render the chart
chart2();
```

## Pull Requests and issues

...are very welcome!
