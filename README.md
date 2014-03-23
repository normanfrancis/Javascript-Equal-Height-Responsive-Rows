A simple jQuery plugin to keep elements the same height, supporting resizing and responsive layouts.

Usage
-----

Download the plugin:
```
wget https://github.com/Sam152/Javascript-Equal-Height-Responsive-Rows/raw/master/grids.js
```

Then invoke the plugin like so:
```
$('.element').responsiveEqualHeightGrid();
```
You must select a every element which will be used in the grids calculation, the elements do not need to be siblings of eachother, therefore both of the following are valid:
```
<div class="wrapper">
	<div class="element">Content</div>
	<div class="element">Content</div>
	<div class="element">Content</div>
</div>
```
```
<div class="wrapper">
	<div class="wrap-element">
		<div class="element">Content</div>
	</div>
	<div class="wrap-element">
		<div class="element">Content</div>
	</div>
</div>
```

Demo
----

You can see a demo in action <a href="http://sam152.github.io/Javascript-Equal-Height-Responsive-Rows/demo.html">here</a>.


Under the Hood
--------------

The grids are packaged with a few different jquery plugins that are used under the hood. To simply make all the selected elements the same height:

```
$('.group-of-elements').equalHeight();
```

Or if you could like the heights to be evaluated on a row-by-row basis, ensuring elements only match the height of elements in their row:

```
$('.group-of-elements').equalHeightGrid(n); // Where n is the number of columns.
```

If you have a responsive layout and need to detect how many columns exist in your layout you can use the following:

```
var $elements = $('.group-of-elements');
var columns = $elements.detectGridColumns();
$elements.equalHeightGrid(columns);
```

If you would like to keep the grids in sync on document ready, window load and resize, you can use the following as a shortcut to the above:

```
$('.group-of-elements').responsiveEqualHeightGrid();
```
