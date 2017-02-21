[<img src="https://cdn.anychart.com/images/logo-transparent-segoe.png?2" width="234px" alt="AnyChart - Robust JavaScript/HTML5 Chart library for any project">](http://www.anychart.com)

React Plugin for AnyChart
=========

Intuitive and easy to use [React](https://facebook.github.io/react/) plugin that allows you to create and work with [AnyChart JavaScript Charts](http://anychart.com).

## Table of Contents

* [Download and Install](#download-and-install)
* [Quick Start](#quick-start)
* [Build](#build)
* [Examples Overview](#examples-overview)
* [Usage](#usage)
* [Contacts](#contacts)
* [Links](#links)
* [License](#license)

## Download and install

#### Package managers

You can install AnyChart-React using **npm**, **bower** or **yarn**:

* `npm install anychart-react`
* `bower install anychart-react`
* `yarn add anychart-react`

#### Direct download

Binaries are in the [dist](https://github.com/AnyChart/AnyChart-React/tree/master/dist) folder.

## Quick Start
Here is a basic sample that shows how to add a chart:

index.html:

```
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <title>Anychart React plugin demo</title>
</head>

<body>
<!-- Mount node for application -->
<div id="root"></div>
<script src="app.min.js"></script>
</body>
</html>
```
Where app.min.js is compiled and bundled script of your application.

app.js:

```
import React from 'react'
import ReactDOM from 'react-dom'
import AnyChart from 'anychart-react.min.js'

ReactDOM.render(
  <AnyChart
    type="pie"
    data={[1, 2, 3, 4]}
    title="Simple pie chart"
  />, document.getElementById('root'));
```

## Build
To build plugin and samples you need to install [gulp](http://gulpjs.com/) if you don't have it installed already.

Please install remaining dependencies using following command
```
npm install
```

#### Building plugin
To compile plugin from source run following command
```
gulp
```

#### Building examples
To compile all examples run following command
```
gulp examples
```

To compile certain example run following command
```
gulp <example_name>
```

Feel free to modify samples, build them and see the results.

#### Note
React Plugin for AnyChart is developed using ES6 syntax. There are `import` and `require` statements in it, so you need a JavaScript bundler (such as [browserify](http://browserify.org/) or [webpack](https://webpack.github.io/) if you want to include it in your app.

## Examples Overview
See these examples to learn how things work:

* **[Chart_with_JSON_Settings](https://github.com/anychart/anychart-react/blob/master/examples/chart_with_json)**: Chart with complex JSON settings.
* **[Charts_with_Controls](https://github.com/anychart/anychart-react/blob/master/examples/charts_with_controls)**: Simple demo with 2 charts. Allows to change title and enable/disable legend.
* **[Geographical_Map](https://github.com/anychart/anychart-react/blob/master/examples/choropleth_map)**: Choropleth map demo.
* **[Data_Streaming](https://github.com/anychart/anychart-react/blob/master/examples/data_streaming)**: Simple data streaming demo.
* **[Simple_Dashboard](https://github.com/anychart/anychart-react/blob/master/examples/simple_dashboard)**: Simple dashboard demo.
* **[Stock Chart](https://github.com/anychart/anychart-react/blob/master/examples/stock)**: Stock chart demo.
* **[Tabs](https://github.com/anychart/anychart-react/blob/master/examples/tabs)**: Demo shows how you can use AnyChart with [React Tabs](https://github.com/reactjs/react-tabs); also shows how to control a legend using component state.

The source code for all examples is in the [`examples/src`](https://github.com/anychart/anychart-react/blob/master/examples/src) folder.

## Usage
Property | Code sample | Description
--- | --- | ---
instance | `<AnyChart instance={myChart}` | Allows to use a [preconfigured instance](https://github.com/anychart/anychart-react/blob/master/examples/src/simple_dashboard.js)
id | `<AnyChart id="chart-container" />` | Container id.
type\* | `<AnyChart type="line" />` | Chart type.
data | `<AnyChart type="column" data={[3, 1, 2]} />` | Chart data.
width/height | `<AnyChart width={800} height={600} />` | Width/height of a chart (stage).
\* - property is required if you do not use an instance.

If you do not use an *instance* property of a component, properties go exactly as they go in [AnyChart JavaScript API](https://api.anychart.com).

For example:

```
<AnyChart type="column" data={[3, 1, 2]} title="My Chart Title" legend="true"/>
```
is equivalent to:

```
var chart = anychart.column([3,1,2]);
chart.title("My Chart Title");
chart.legend(true);
```

#### Multiple entities (axes, line markers, grids)
To configure entity by index, you should use an array as a value: the first item in an array - index of an entity, the second - configuration.

```
<AnyChart yAxis={[1, {enabled: true}]} />
```

Such settings are shown in [Chart_with_JSON Settings](https://github.com/anychart/anychart-react/blob/master/examples/src/chart_with_json.js) example.

## Contacts

* Web: [www.anychart.com](http://www.anychart.com)
* Email: [contact@anychart.com](mailto:contact@anychart.com)
* Twitter: [anychart](https://twitter.com/anychart)
* Facebook: [AnyCharts](https://www.facebook.com/AnyCharts)
* LinkedIn: [anychart](https://www.linkedin.com/company/anychart)

## Links

* [Report Issues](https://github.com/AnyChart/AnyChart-React/issues)
* [AnyChart Website](http://www.anychart.com)
* [Download AnyChart](http://www.anychart.com/download/)
* [AnyChart Licensing](http://www.anychart.com/buy/)
* [AnyChart Support](http://www.anychart.com/support/)
* [AnyChart Playground](http://playground.anychart.com)
* [AnyChart Documentation](http://docs.anychart.com)
* [AnyChart API Reference](http://api.anychart.com)
* [AnyChart Sample Solutions](http://www.anychart.com/solutions/)
* [AnyChart Integrations](http://www.anychart.com/integrations/)

## License

[© AnyChart.com - JavaScript charts](http://www.anychart.com). React Plugin is released under the [Apache 2.0 License](https://github.com/AnyChart/AnyChart-React/blob/master/LICENSE).
