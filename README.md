SassyGradients
==============

Sass helpers to manipulate gradients.

## Instanciate

```scss
$gradient: sg-gradient(to bottom right, red 20%, yellow, green, blue 55%, red 55%, green);
```

## Display

```scss
.selector {
  @include sg-display($gradient);
}
```

```css
.selector {
  background: red;
  background: linear-gradient(to bottom right, red 20%, yellow 31.6666666667%, green 43.3333333333%, blue 55%, red 55%, green 100%);
}
```

## Access properties

```scss
$fallback: sg-get($gradient, "fallback");
// red

$direction: sg-get($gradient, "direction");
// to bottom right

$legacy-direction: sg-get($gradient, "legacy-direction");
// top left

$colors: sg-get($gradient, "colors"):
// red, yellow, green, blue, red, green

$color-stops: sg-get($gradient, "color-stops");
// red 20%, yellow 31.6666666667%, green 43.3333333333%, blue 55%, red 55%, green 100%

$length: sg-get($gradient, "length");
// 6
```

## Debug

```scss
.debug {
  @include gh-debug($gradient);
}
```

```css
@debug-gradient {
  raw-debug: ("fallback": red, "direction": to bottom right, "legacy-direction": top left, "color-stops": (red 20%, yellow 31.6666666667%, green 43.3333333333%, blue 55%, red 55%, green 100%), "colors": (red, yellow, green, blue, red, green), "length": 6);
  fallback: red;
  direction: to bottom right;
  legacy-direction: top left;
  color-stops: red 20%, yellow 31.6666666667%, green 43.3333333333%, blue 55%, red 55%, green 100%;
  colors: red, yellow, green, blue, red, green;
  length: 6;
}
```
