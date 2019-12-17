---
layout: post
title:  "A Comprehensive Guide to Visualization Using ECharts"
date:   2019-12-17
excerpt: "Just about everything you'll need to visualize your data with ECharts"
tag:
- echarts 
- visualization
- P2P
- heatmap
- javascripts
- npm
- parcel
comments: true
project: true
feature: https://user-images.githubusercontent.com/26131764/70916681-0bc62500-2057-11ea-87a7-2b49ba113509.png
---

This is a comprehensive step-by-step tutorial on how to visualize data with ECharts. Special thinks to [Wenhe Li](https://portfolio.steins.live) for the help in website building.

Live Demo of a P2P default geomap: [link](honors.anpu.li)

## Installation & Setup

### Install node.js

Please go to the [download page](https://nodejs.org/en/download/) of the official website and follow the instructions.

### Install ECharts

First, make a new directory where you want to put your visualization in.

```shell
mkdir echarts-vis
cd echarts-vis
```

Second, make a new file called `package.json` and copy the following in the file. Please ignore the meaning for now if you don't understand what this does. Save and close the file.

```json
{
    "scripts": {
        "start": "npx parcel index.html"
    }
}
```

Third, run the following command

```shell
npm install --save echarts
npm install --save-dev parcel
```

## Build Your First Visualization: Bar

This section will walk you through a simple bar graph.

![image](https://user-images.githubusercontent.com/26131764/70975935-e2080f00-20e5-11ea-9163-1b0903817dde.png)

### Prepare html file

Create a new file `index.html`. Copy the following content inside

```html
<!DOCTYPE html>
<html>
<head>
    <meta charset="utf-8">
    <title>ECharts</title>
</head>
<body>
    <!-- Prepare a Dom for ECharts -->
    <div id="main" style="width: 600px;height:400px;"></div>

    <script src="index.js"></script>
</body>
</html>
```

### Prepare js file

Create a new file `index.js`

```javascript
import * as echarts from "echarts";

// based on the prepared dom, initiate an echarts instance
var myChart = echarts.init(document.getElementById('main'));

// specify configuration and data
var option = {
    title: {
        text: 'ECharts Demo'
    },
    tooltip: {},
    legend: {
        data:['Sales']
    },
    xAxis: {
        data: ["Shirts","Cardigan","Sweater","Pants","High Heels","Socks"]
    },
    yAxis: {},
    series: [{
        name: 'Sales',
        type: 'bar',
        data: [5, 20, 36, 10, 10, 20]
    }]
};

// Use the config and data set above to show the graph
myChart.setOption(option);
```

### Build

Please run

```shell
npm run start
```

Wait a few moments and you should see

![image](https://user-images.githubusercontent.com/26131764/70975659-53938d80-20e5-11ea-8fa0-19c318c31251.png)

You can can open <http://localhost:1234> and play with the interaction.
