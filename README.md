# Basic Tool for Plotting Bar Charts using D3

# Basic Usage:

- `npm install -S bar-plot-d3`

- import in code
  - `import 'd3Bar from 'bar-plot-d3'`
- Add canvas element to html page (d3Canvas is the default id expected)
  - `<div id='#d3Canvas'>`

- Call addBars
  - `const data_example = [{country: 'USA': 20.8}, {country: 'China': 14.9}, {country: 'Japan': 4.9}, {country: 'Germany': 3.8}, {country: 'France': 2.6}]`
  - `d3Bar.addBars({data: data})`

  # Options:

- specify canvas size (defaults to 900 x 600)
  - (automatically adjusts size to fit canvas)
  - `d3Bar({data: data, canvasHeight: 500, canvasWidth: 800})`

- check default settings
  - `var defaults = d3Bar.checkDefaults()`
  - you can also check if you have customized the canvas size
  - `var defaults = d3Bar.checkDefaults({canvasHeight: 500, canvasWidth: 800})`
