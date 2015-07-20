# lazygrid

Simple Stylus. Clean markup. Nap time.


### Installation

`@import 'path/to/lazygrid.styl'`


### Usage

You can set your global gutter in `lazygrid.styl`, or set gutters on a per area (row gutters need to match cells) basis.

- `g-row($gut = $gutter)` - Create a row to hold cells.
- `g-cell($frac = 1, $gut = $gutter)` - Set the size (width) of your cell. Accepts a fraction as its first param.

```html
<div class="row">
  <div class="cell">1</div>
  <div class="cell">2</div>
  <div class="cell">3</div>
</div>
```

```stylus
.row
	g-row()

.cell
	g-cell(1/3)
```

- `g-equal($gut = $gutter)` - Create a row of cells with equal width. Add as many or few as you want.

```html
<div class="equal">
	<div>1</div>
  <div>2</div>
  <div>3</div>
</div>
```

```stylus
.equal
  g-equal()
```

- `g-move($frac = 0, $gut = $gutter)` - Source ordering. Pass positive or negative fractions as the first param to "shift" elements left and right for various devices.
- `g-background($color = red, $gut = $gutter)` - Apply to a row to give it a background. Otherwise you'll get backgrounds that aren't flush with the cells contained within.
- `g-align($dir = left)` - Align cells to their containing row. Options are:
	- `left`
	- `center`
	- `right`
	- `top`
	- `middle`
	- `bottom`
	- `both`
- `g-offset($frac = 0, $gut = $gutter)` - Offset a cell from another cell. Pass a positive or negative fraction to offset in different directions.

