Awesome Bootstrap Checkbox
==========================
[![NPM version](https://img.shields.io/npm/v/awesome-bootstrap-checkbox.svg?style=flat)](https://www.npmjs.com/package/awesome-bootstrap-checkbox)
[![NPM downloads](https://img.shields.io/npm/dm/awesome-bootstrap-checkbox.svg?style=flat)](https://www.npmjs.com/package/awesome-bootstrap-checkbox)
[![Dependency Status](https://img.shields.io/david/dev/flatlogic/awesome-bootstrap-checkbox.svg?branch=master&style=flat)](https://www.npmjs.com/package/awesome-bootstrap-checkbox)

[Font Awesome][] [Bootstrap][] Checkboxes & Radios plugin. Pure CSS way to make inputs look prettier. **No Javascript!**

Now with **[Bootstrap 4][]** support!

**[Demo][]**

Use
------------

First just include **awesome-bootstrap-checkbox.css** somewhere in your HTML, or add the equivalent files to your [Sass](#using-sass) configuration.
Next, everything is based on code convention. Here is checkbox markup from Bootstrap site:

````html
<form role="form">
  ...
  <div class="form-check">
    <label class="form-check-label">
      <input class="form-check-input" type="checkbox">
      Check me out
    </label>
  </div>
  ...
</form>
````

We have to alter it a bit:
````html
<form role="form">
  ...
  <div class="form-check abc-checkbox abc-checkbox-primary">
    <input class="form-check-input" id="checkbox1" type="checkbox">
    <label class="form-check-label" for="checkbox1">
      Check me out
    </label>
  </div>
  ...
</form>
````
That's it. It will work. But it **will not** work if you nest input inside label or put label before input.

Browser support
-----------
- Firefox (_3.6+_)
- Chrome  (_14+_)
- IE      (_9+_)
- Opera   (_11.6+_)
- Safari  (_6+_)

Radios
------------

It's the same for radios. Markup has to be the following:
````html
<form role="form">
  ...
  <div class="form-check abc-radio abc-radio-primary">
    <input class="form-check-input" type="radio" name="radio1" id="radio1" value="option1" checked>
    <label class="form-check-label" for="radio1">
      One
    </label>
  </div>
  <div class="form-check abc-radio abc-radio-primary">
    <input class="form-check-input" type="radio" name="radio1" id="radio2" value="option2">
    <label class="form-check-label" for="radio2">
      Two
    </label>
  </div>
  ...
</form>
````

Brand Colors and other features
------------

You may use `abc-checkbox-primary`, `abc-checkbox-danger`, `abc-radio-info`, etc to style checkboxes and radios with brand bootstrap colors.

`abc-checkbox-circle` is for rounded checkboxes.

Inputs without label text:

````html
<div class="form-check abc-checkbox">
  <input class="form-check-input" type="checkbox" id="singleCheckbox" value="option1" aria-label="Single checkbox One">
  <label class="form-check-label" for="singleCheckbox"></label>
</div>
````

Using [Sass][]
----------

As per example in the `demo` folder, to use Awesome Bootstrap Checkbox you'll have to `@import` the following library parts:

````scss
@import "../node_modules/bootstrap/scss/functions";
@import "../node_modules/bootstrap/scss/variables";
@import "../node_modules/bootstrap/scss/mixins";

// Font Awesome 4
@import "../node_modules/Font-Awesome/scss/variables";

// Font Awesome 5 (Free)
@import "node_modules/@fortawesome/fontawesome-free/scss/fontawesome";
@import "node_modules/@fortawesome/fontawesome-free/scss/solid";

@import "../awesome-bootstrap-checkbox";
````

Adjust this to the path where your bootstrap and font-awesome files are located.

For Font Awesome 5 Free you will need to specify the correct font family:

Font Awesome 5 Free
------------
````scss
$font-family-icon: 'Font Awesome 5 Free';
$check-icon: "\f00c";
````
If you want to use another icon font instead of Font Awesome, such as [Glyphicons][], override the default variables:

Glyphicons
------------
````scss
$font-family-icon: 'Glyphicons Halflings';
$check-icon: "\e013";

.abc-checkbox label:after {
    padding-left: 4px;
    padding-top: 2px;
    font-size: 9px;
}
````

Or for plain CSS, override the `.abc-checkbox` class:
````css
.abc-checkbox input[type=checkbox]:checked + label:after {
    font-family: 'Glyphicons Halflings';
    content: "\e013";
}

.abc-checkbox label:after {
    padding-left: 4px;
    padding-top: 2px;
    font-size: 9px;
}
````

Credits
------------

Based on the [Bootstrap][] and the awesome [Font Awesome][].


[Demo]: https://flatlogic.github.io/awesome-bootstrap-checkbox/demo/1.0.0/
[Bootstrap]: https://getbootstrap.com/docs/3.4/
[Bootstrap 4]: https://getbootstrap.com/
[Font Awesome]: https://github.com/FortAwesome/Font-Awesome
[Glyphicons]: https://getbootstrap.com/components/#glyphicons
[Sass]: https://sass-lang.com/
[Less]: http://lesscss.org/
