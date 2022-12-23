![App Screenshot](https://github.com/Huiclaire/JavaScript30/blob/master/08-Fun_with_HTML5_Canvas/images/js30-day8.png)

# 08- Array Cardio Day 2
Have dynamic fun in a HTML5 Canvas.

## Demo
view demo [here](https://huiclaire.github.io/JavaScript30/08-Fun_with_HTML5_Canvas/index-Claire.html)

## Lesson learned

### Canvas

- Properties used in the lesson:
  -  `ctx.lineCap`: the shape of the stroke, `round` | `butt` | `square`.
  -  `ctx.lineJoin`: determines how two connecting segments (of lines, arcs or curves) with non-zero lengths in a shape are joined together), `bevel` | `round` | `miter`.
  -  `ctx.lineWidth`: sets the thickness of lines in space units.
  - `ctx.strokeStyle`: specifies the color or style to use for the lines around shapes. The default is `#000` (black).
  - `ctx.fillStyle`: specifies the color or style to use inside shapes. The default is `#000` (black).

- Methods
  - `ctx.beginPath()`: starts a new path by emptying the list of sub-paths. Call this method when you want to create a new path.
  - `ctx.stroke()`: strokes the current or given path with the current stroke style using the non-zero winding rule.
  - `ctx.moveTo()`: moves the starting point of a new sub-path to the (x, y) coordinates.
  - `ctx.lineTo()`: connects the last point in the sub-path to the x, y coordinates with a straight line(but does not actually draw it).


### HSL

[mothereffinghsl.com](http://mothereffinghsl.com/) website shows you the figure of HSL.
The [HSL](https://developer.mozilla.org/en-US/docs/Web/CSS/color_value)(seel the "hsl()" section) is the Hue-saturation-lightness model using the `hsl()` function notation.

The HSL color model defines a given color in the sRGB color space according to its hue, saturation, and lightness components. Many designers find HSL more intuitive than RGB, since it allows hue, saturation, and lightness to each be adjusted independently.
