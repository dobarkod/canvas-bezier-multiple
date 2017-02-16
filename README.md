JavaScript utility function for drawing cubic Bezier curves through multiple
points on a HTML5 canvas.

For background and theory, see https://goodcode.io/articles/bezier-canvas/

## Installation

Copy the `src/canvas-bezier-multipoint.js` file directly into your project.

## Usage

To draw the curve, call the function with the drawing context and points
to draw through. Points should be specified as array of pairs, where each
pair is (x,y) coordinate of the point in the canvas:

Example usage:

    var canvas = document.getElementById('mycanvas'),
        ctx = canvas.getContext('2d'),
        points = [[10, 10], [100, 10], [100, 100], [200, 100]];

    bezierCurveThrough(ctx, points);

To tweak the tension (how "tight" are the bends in the curve), pass the
third parameter:

    bezierCurveThrough(ctx, point, 0.5);

The default tension value is 0.25.

## Demo

A simple demo is available in `demo/index.html`.

## Copyright and license

Copyright &copy; 2017 Good Code and canvas-bezier-multipoint contributors.

You can use and/or distribute this software under the terms of MIT license
specified in `LICENSE.md`.
