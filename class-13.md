# Chart.js

#### Setting up:

        <!DOCTYPE html>
        <html lang="en">
            <head>
                <meta charset="utf-8" />
                <title>Chart.js demo</title>
                <script src='Chart.min.js'></script>
            </head>
            <body>
            </body>
        </html>

#### Drawing a line chart:

        <canvas id="buyers" width="600" height="400"></canvas>

**You can use the link when you needed for it [Chart.js docs](https://www.chartjs.org/docs/latest/)**


## Creating a Chart
* It's easy to get started with Chart.js. All that's required is the script included in your page along with a single `<canvas>` node to render the chart.

## Contributing
* Before submitting an issue or a pull request to the project, please take a moment to look over the contributing guidelines first.
    * Joining the project
    * Building and Testing
    * Documentation
    * Image-Based Tests
    * Bugs and Issues

## License
* Chart.js is available under the [MIT license](https://opensource.org/licenses/MIT).
* Documentation is copyright © 2014-2021 Chart.js contributors.


# Basic usage of canvas
 ### The `<canvas>` element

        <canvas id="tutorial" width="150" height="150"></canvas>

 ### Fallback content

        <canvas id="stockGraph" width="150" height="150">
        current stock price: $3.15 + 0.15
        </canvas>

        <canvas id="clock" width="150" height="150">
        <img src="images/clock.png" width="150" height="150" alt=""/>
        </canvas>

 ### Required `</canvas>` tag
 ### The rendering context

        var canvas = document.getElementById('tutorial');
        var ctx = canvas.getContext('2d');

### Checking for support

        var canvas = document.getElementById('tutorial');

        if (canvas.getContext) {
        var ctx = canvas.getContext('2d');
        // drawing code here
        } else {
        // canvas-unsupported code here
        }

### A skeleton template

---
---

### Drawing shapes with canvas
### The grid
### Drawing rectangles
* Rectangular shape example

        function draw() {
        var canvas = document.getElementById('canvas');
        if (canvas.getContext) {
            var ctx = canvas.getContext('2d');

            ctx.fillRect(25, 25, 100, 100);
            ctx.clearRect(45, 45, 60, 60);
            ctx.strokeRect(50, 50, 50, 50);
        }
        }

### Drawing paths
1. First, you create the path.
2. Then you use [drawing commands](https://developer.mozilla.org/en-US/docs/Web/API/CanvasRenderingContext2D#paths) to draw into the path.
3. Once the path has been created, you can stroke or fill the path to render it.

* functions used to perform these steps:
    * beginPath()
    * closePath()
    * stroke()
    * fill()


### Drawing a triangle

        function draw() {
        var canvas = document.getElementById('canvas');
        if (canvas.getContext) {
            var ctx = canvas.getContext('2d');

            ctx.beginPath();
            ctx.moveTo(75, 50);
            ctx.lineTo(100, 75);
            ctx.lineTo(100, 25);
            ctx.fill();
        }
        }

### Moving the pen

> `moveTo(x, y)`

        function draw() {
        var canvas = document.getElementById('canvas');
        if (canvas.getContext) {
            var ctx = canvas.getContext('2d');

            ctx.beginPath();
            ctx.arc(75, 75, 50, 0, Math.PI * 2, true); // Outer circle
            ctx.moveTo(110, 75);
            ctx.arc(75, 75, 35, 0, Math.PI, false);  // Mouth (clockwise)
            ctx.moveTo(65, 65);
            ctx.arc(60, 65, 5, 0, Math.PI * 2, true);  // Left eye
            ctx.moveTo(95, 65);
            ctx.arc(90, 65, 5, 0, Math.PI * 2, true);  // Right eye
            ctx.stroke();
        }
        }


### Lines

> `lineTo(x, y)`

        function draw() {
        var canvas = document.getElementById('canvas');
        if (canvas.getContext) {
            var ctx = canvas.getContext('2d');

            // Filled triangle
            ctx.beginPath();
            ctx.moveTo(25, 25);
            ctx.lineTo(105, 25);
            ctx.lineTo(25, 105);
            ctx.fill();

            // Stroked triangle
            ctx.beginPath();
            ctx.moveTo(125, 125);
            ctx.lineTo(125, 45);
            ctx.lineTo(45, 125);
            ctx.closePath();
            ctx.stroke();
        }
        }


### Arcs
> `arc()` or `arcTo()`

### Cubic Bezier curves

        function draw() {
        var canvas = document.getElementById('canvas');
        if (canvas.getContext) {
            var ctx = canvas.getContext('2d');

            // Cubic curves example
            ctx.beginPath();
            ctx.moveTo(75, 40);
            ctx.bezierCurveTo(75, 37, 70, 25, 50, 25);
            ctx.bezierCurveTo(20, 25, 20, 62.5, 20, 62.5);
            ctx.bezierCurveTo(20, 80, 40, 102, 75, 120);
            ctx.bezierCurveTo(110, 102, 130, 80, 130, 62.5);
            ctx.bezierCurveTo(130, 62.5, 130, 25, 100, 25);
            ctx.bezierCurveTo(85, 25, 75, 37, 75, 40);
            ctx.fill();
        }
        }

### Path2D objects

        function draw() {
        var canvas = document.getElementById('canvas');
        if (canvas.getContext) {
            var ctx = canvas.getContext('2d');

            var rectangle = new Path2D();
            rectangle.rect(10, 10, 50, 50);

            var circle = new Path2D();
            circle.arc(100, 35, 25, 0, 2 * Math.PI);

            ctx.stroke(rectangle);
            ctx.fill(circle);
        }
        }

### Using SVG paths

        var p = new Path2D('M10 10 h 80 v 80 h -80 Z');

### Applying styles and colors

### Colors
*  can use: `fillStyle` and `strokeStyle`.

### Line styles

        lineWidth = value
        lineCap = type
        lineJoin = type
        miterLimit = value
        getLineDash()
        setLineDash(segments)
        lineDashOffset = value

### A lineCap example

        butt, round and square

### A lineJoin example

        round
        bevel
        miter

**You can use the link when you needed for it [Applying styles and colors](https://developer.mozilla.org/en-US/docs/Web/API/Canvas_API/Tutorial/Applying_styles_and_colors)**


### Drawing text

        fillText(text, x, y [, maxWidth])
        strokeText(text, x, y [, maxWidth])

### Styling text

        font = value
        textAlign = value
        textBaseline = value
        direction = value

### Advanced text measurements

        measureText()   

**You can use the link when you needed for it [Drawing text](https://developer.mozilla.org/en-US/docs/Web/API/Canvas_API/Tutorial/Drawing_text)**