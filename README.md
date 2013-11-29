d3-funnel-charts
================

A funnel chart implementation using d3.js

Usage
=====
To begin, you must instantiate a FunnelChart.  FunnelChart objects have four parameters: data, width, height, and bottomPct.  Data is the only required parameter.

`data` = an array containing arrays of categories and engagement in order from greatest expected funnel engagement to lowest.  

`width` & `height` = width & height of chart (default is 400 and 600)

`bottomPct` = the percentage of the width the bottom base of the funnel trapezoid takes up.  The top base always takes up the entire width, but the percentage of the total width that the bottom base takes up can be changed.  (default = 1/3)

To actually draw the FunnelChart, call the `draw` method of the FunnelChart.  The draw method takes in a selector for an elementthat the FunnelChart should be drawn in and a speed (default = 2.5).

Example:

    <div id="funnelContainer"></div>
    <script src="d3.min.js"></script> // Make sure to include d3.js first
    <script src="d3-funnel-charts.min.js"></script>
    <script type="text/javascript">
        data = [['Video Views', 1500], ['Comments', 300], ['Video Responses', 150]];
        chart = new FunnelChart(data, 650, 450, 1/4);
        chart.draw('#funnelContainer', 2);
    </script>
  
A demo of the above example can be found [here](http://smithamilli.com/funnel-charts-in-d3-js/)
