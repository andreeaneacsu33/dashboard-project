# Bar Chart React Component

This is a web component that displays a bar chart based on the data given as input.\
To start the server in the development mode, run `npm start` in the project directory and navigate to `http://localhost:3000` in your web browser.\
The page will reload if you make edits and you will also see any lint errors in the console.

## Use

The Bar Chart is composed of two axis, AxisX and AxisY and several Bar components that are the representation of the data given as input.
You can locate these in `src/components` directory.

To use the Bar Chart component, you have to import it:
``` jsx harmony
import BarChart from "./components/BarChart";
```

and prepare your data:
```jsx harmony
const data = [
            ["Mon", 20],
            ["Tue", 14],
            ["Wed", 12],
            ["Thu", 4],
            ["Fri", 5],
            ["Sat", 18],
            ["Sun", 0],
        ];
const xLabel='Day';
const yLabel='km';
const width=450;
const height=350;
```

To render the component in your page, use the \<BarChart /> tag with your custom data:

```jsx harmony
<BarChart
   data={data}
   xLabel={xLabel}
   yLabel={yLabel}
   width={width}
   height={height}
/>
```

## Example

![Bar Chart Component](https://github.com/andreeaneacsu33/bar-chart-component/blob/master/public/bar-chart-component.png?raw=true)

## Properties
|Property | Type | Description
:---: | :---: | :---:
width| number | Width of the bar chart in px
height| number | Height of the bar chart in px
xLabel| string | Label for the Ox axis
yLabel| string | Label for the Oy axis
data| array | Array of pairs containing (Ox,Oy) data

## Code explanation
The implementation uses SVG (Scalable Vector Graphics) in order to group the rectangles, lines and texts and obtain the bar chart. The properties `width` and `height` are used to set the size of the chart and, based on these, further computations are made. In the BarChart.js file you can see that a \<svg> tag holds all the components of the chart, having the width and height given by the user. Before rendering the AxisX, AxisY and the Bars, the data is prepared. For example: the length of the axis Ox and Oy, the width of a bar, the minimum and maximum value (that results in the length of the bar), etc.\




