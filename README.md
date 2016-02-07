# D3 Sparkline Chart

![Reusable D3.js Sparkline chart](https://raw.githubusercontent.com/DKirwan/reusable-d3-sparkline/develop/thumbnail.png)

This chart was built with Mike Bostock's [reusable D3.js charts best practice](http://bost.ocks.org/mike/chart/) in mind.

## How to use

1: Load the sparkline.js code
`<script src="path/to/sparkline.js"></script>`

2: Then configure the chart and render it
```javascript
var chart1 = sparkline()
              .width(155)
              .height(50)
              .gradientColors(['green', 'orange', 'red']) // top -> bottom
              .csvFilePath('data1.csv') // relative to sparkline.js
              .selector('#chart1-selector');
var chart2 = sparkline()
              .width(155)
              .height(50)
              .gradientColors(['green', 'orange', 'red']) // top -> bottom
              .csvFilePath('data2.csv') // relative to sparkline.js
              .selector('#chart2-selector');
chart1();  // render the chart
chart2();
```

## Pull Requests and issues

...are very welcome!
