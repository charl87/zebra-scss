[![GitHub version](https://badge.fury.io/gh/swillis93%2Fzebra.svg)](https://badge.fury.io/gh/swillis93%2Fzebra)

# Zebra - a customizable CSS grid system
Just like a Zebra's stripes, every website is unique, and so we've created a grid system that can be tailored to your individual project requirements.

## Getting started
It's really easy to get started with Zebra, either include the `/dist/css/zebra.css` file in your `<head>`, or copy the `/src/sass/_zebra.scss` and `/src/sass/_zebra-settings.scss` files into your SASS project to take advantage of Zebra's customization options.
```html
<!-- Add this to your head -->
<link rel="stylesheet" type="text/css" href="/css/zebra.css">

<!-- OR copy the _zebra files into your SASS project and add this to your site.scss -->
@import '/src/sass/_zebra'
```
*Remember to update the file paths to match your project structure.*

Now you just need to create an element with the class of `row` and add your columns within.
```css
<div class="row">
	<div class="col--2of12">A column that spans 2/12 of the parent</div>
	<div class="col--6of12">A column that spans 6/12 of the parent</div>
	<div class="col--4of12">A column that spans 4/12 of the parent</div>
</div>
```

For a more detailed usage guide, see the [wiki][wiki].

## What is Zebra?
Zebra is a CSS grid system based on the [BEM][bem] methodology, that can be customized through the modification of built in SASS variables.

Zebra then provides you with a varying number of CSS classes (depending on what [settings][settings] you choose).

Base columns follow a slightly simplified version of the BEM methodology, combining the properties of `.col` (a block) with it's size `.col--XofX` (a modifier). This is done for a couple of reasons; 

1. Firstly, there should never be an instance where a column element doesn't have a size modifer, as this would result in a column with no width.
2. Secondly, this helps to keep the DOM cleaner, as there are less classes littering each element.

```css
<div class="col--1of2">Zebra's simplified column classes</div>
<div class="col col--1of2">Typical BEM usage</div>
```



[settings]: https://github.com/swillis93/zebra/wiki/Settings
[bem]: http://getbem.com/introduction
[wiki]: https://github.com/swillis93/zebra/wiki