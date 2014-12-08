Terminology
===========

## Gradient

Gradient instance, resulting of a `sg-gradient` call.

```scss
// Example
$gradient: (
  "fallback": red,
  "direction": to bottom right,
  "legacy-direction": top left,
  "color-stops": (red 20%, yellow 31.6666666667%, green 43.3333333333%, blue 55%, red 55%, green 100%),
  "colors": (red, yellow, green, blue, red, green),
  "length": 6
);
```

## Color

Value whom type is `color`.

```scss
// Example
$color: hotpink;
```

## Stop

Length that comes with a color in a color-stop. Usually expressed in `%` but can be any unit.

```scss
// Example
$stop: 42%;
```

## Color-stop

Breakpoint used in a gradient. Consists on a color which may or may not come with a stop, separated with a space.

```scss
// Example
$color-stop: hotpink;
$color-stop: hotpink 42%;
```

## Full color-stop

Color-stop composed of a color **and** a stop.

```scss
// Example
$color-stop: hotpink 42%;
```

## Fallback

When related to gradients, the fallback is the color being used before any linear-gradient declaration for browsers that do not support CSS gradients.

```scss
.selector {
    background: hotpink;
    background: linear-gradient(to right, hotpink, tomato);
}
