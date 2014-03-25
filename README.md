d3-funnel-charts
================

A funnel chart implementation using d3.js

Usage
=====
To begin, you must instantiate a FunnelChart.  FunnelChart objects have four parameters: data, width, height, and bottomPct.  Data is the only required parameter.

`data` = an array containing arrays of categories and engagement in order from greatest expected funnel engagement to lowest.  

`width` & `height` = width & height of chart (default is 400 and 600)

`bottomPct` = the percentage of the width the bottom base of the funnel trapezoid takes up.  The top base always takes up the entire width, but the percentage of the total width that the bottom base takes up can be changed.  (default = 1/3)

To actually draw the FunnelChart, call the `draw` method of the FunnelChart.  The draw method takes in a [selector](https://github.com/mbostock/d3/wiki/Selections) for an element that the FunnelChart should be drawn in and a speed (default = 2.5).  Make sure that you already have an element that corresponds to the selector you use because d3-funnel-charts doesn't create elements; it just uses an element you already have in your HTML as a container.

Example:

    <div id="funnelContainer"></div>
    <script src="d3.min.js"></script> // Make sure to include d3.js first
    <script src="d3-funnel-charts.min.js"></script>
    <script type="text/javascript">
        var data = [['Video Views', 1500], ['Comments', 300], ['Video Responses', 150]];
        var chart = new FunnelChart(data, 650, 450, 1/4);
        chart.draw('#funnelContainer', 2);
    </script>
  
A demo of the above example can be found [here](http://smithamilli.com/blog/funnel-charts-in-d3.js/)

License
======
MIT
