# Basic Tool for Plotting Bar Charts using D3

# Basic Usage:

- `npm install -S bar-plot-d3`

- import in code
  - `import 'd3Bar from 'bar-plot-d3'`
- Add canvas element to html page (d3Canvas is the default id expected)
  - `<div id='#d3Canvas' />`

- Call addBars
  - `const data_example = [{country: 'USA': gdp: 20.8}, {country: 'China': gdp: 14.9}, {country: 'Japan': gdp: 4.9}, {country: 'Germany': gdp: 3.8}, {country: 'France': gdp: 2.6}]`
  - `d3Bar.addBars({data: data})`

  # Options:

- specify canvas size (defaults to 900 x 600)
  - (automatically adjusts size to fit canvas)
  - `d3Bar({data: data, canvasHeight: 500, canvasWidth: 800})`

- specify orientation (defaults to vertical bar chart)
  - (automatically adjusts size to fit canvas)
  - `d3Bar({data: data, orientation: "horizontal"})`

- specify axis labels
  - (automatically adjusts size to fit canvas)
  - `d3Bar({data: data, xaxis: 'Country', yaxis: 'GDP ($USD in millions)'})`

- specify scale
  - (overrides auto-scaling that fits plot to canvas size)
  - `d3Bar({data: data, scale: 10})`

- check default settings
  - `var defaults = d3Bar.checkDefaults()`
  - this allows you to check values like 'scale', 'maxValue' etc. if you have customized the canvas size and/or scaling
  - `var defaults = d3Bar.checkDefaults({data: data, scale: 10, canvasHeight: 500, canvasWidth: 800})`

- embed data table in page
  - add empty element in html
  - `<div#embedDataHere />`
    - `d3Bar.addBars({data: data, embedData: "embedDataHere"})`
