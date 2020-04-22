# D3 Animated Bar Chart

## HTML
This bar chart is split up into 2 main areas - `dashboard` and `chart`.

### Dashboard
This comprises of two drop-down lists - `ddlStat` and `ddlYear`. They are populated using data from the `graphData` object. Upon value being changed, they will call the `setData()` method of the `config` object.

### Chart
This is in turn split into four SVGs
- `scale` provides measurements at calculated intervals. These intervals are calculated based on the maximum statistic value in the *graphData* object. Tags inserted into the scale SVG are line and text.
- `chart` holds the bars of the chart, the data values background lines and `mean` line. Tags inserted into the chart SVG are rect, line and text.
- `filler` is the space bottom of `scale` and left of `legend`. It is merely meant to help align the chart.
- `legend` holds the data labels. Tags inserted are text.
- Other notes...
  - width of `chart` and `legend` should be equal.
  - height of `scale` and `chart` should be equal.
  - width of `scale` and `filler` should be equal.
  - height of `filler` and `legend` should be equal.

## JavaScript
The script is mainly split into two parts - `graphData` and `config`.

### The *graphData* object
This holds the data, which is an array of objects, followed by an array of statistic types and an array of years. The latter two are meant to populate the `ddlStat` and `ddlYear` drop-down lists respectively.

The first array holds objects which show football players and their appearances and goals for each given year.

### The *config* object
This is for processing data. There are methods for calculating chart height, chart width, max, mean and finally, displaying the appropriate data.

Properties will hold values for scaling of chart, width and height of chart parts, and so on.
