# dashing-analog-clock

A beautiful analog clock for [Dashing](http://shopify.github.com/dashing).

## Preview

![AnalogClock](https://raw.githubusercontent.com/wiki/jorgemorgado/dashing-analog-clock/analog-clock.png)

## Description

Displays a beautiful analog clock setting at local time. The clock can be
scaled to whatever width x height you have defined your widget.

The clock itself was taken from CSS-Tricks [Clock](https://css-tricks.com/css3-clock/).
All I've done was mostly port the code to Dashing, make it scalable to better
fit the widget base dimensions and adjust the images for the new sizes.

## Usage

Create the directory `widgets/analog_chart` and copy this widget's files
into that folder.

Copy the images folder `analog_clock` into the `assets/images` folder.

Add the following code on the desired dashboard:

```erb
<li data-row="1" data-col="1" data-sizex="1" data-sizey="1">
    <div data-view="AnalogClock"></div>
</li>
```

That's it!! Your new Dashing clock will rock!

If you want to make it bigger, change the widget data-sizex/sizey dimensions.
Example:

```erb
<li data-row="1" data-col="1" data-sizex="2" data-sizey="2">
    <div data-view="AnalogClock"></div>
</li>
```

And increase the clock's width on the CSS file (the default is 300px).
Example:

```scss
$clock-width:       600px;
```

Reload your dashboard and you're done.

*NOTE:* I've left the original `clockface.jpg` image in the folder. This image
has a smooth shadow and it works quite well in case you want to have a
white background-color for your clock (no transparency). In this case, don't
forget to change the clock's background URL image in the styles:

```css
background: url(analog_clock/clockface.jpg);
```

## Contributors

- [Jorge Morgado](https://github.com/jorgemorgado)
- Analog clock from [Clock](https://css-tricks.com/css3-clock/)

## License

This widget is released under the [MIT License](http://www.opensource.org/licenses/MIT).
