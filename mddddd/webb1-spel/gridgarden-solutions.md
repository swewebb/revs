# Grid Garden

## Nivå 1

```css
#water {
    grid-column-start: 3;
}
```

## Nivå 2

```css
#poison {
    grid-column-start: 5;
}
```

## Nivå 3

```css
#water {
  grid-column-start: 1;
  grid-column-end: 4;
}
```

## Nivå 4

```css
#water {
  grid-column-start: 1;
  grid-column-end: 2;
}
```

## Nivå 5

```css
#water {
  grid-column-start: 1;
  grid-column-end: -2;
}
```

## Nivå 6

```css
#poison {
    grid-column-start: -3;
}
```

## Nivå 7

```css
#water {
  grid-column-start: 2;
  grid-column-end: span 2;
}
```

## Nivå 8

```css
#water {
  grid-column-start: 1;
  grid-column-end: span 5;
}
```

## Nivå 9

```css
#water {
  grid-column-start: span 3;
  grid-column-end: 6;
}
```

## Nivå 10

```css
#water {
    grid-column: 4 / -1;
}
```

## Nivå 11

```css
#water {
    grid-column: 2/5;
}
```

## Nivå 12

```css
#water {
    grid-row-start: 3;
}
```

## Nivå 13

```css
#water {
    grid-row: 3/-1;
}
```

## Nivå 14

```css
#poison {
    grid-row: -2;
    grid-column: 2;
}
```

## Nivå 15

```css
#water {
    grid-row: 1/-1;
    grid-column: 2/-1;
}
```

## Nivå 16

```css
#water {
    grid-area: 1/2 / 4/-1;
    /* grid-row-start/grid-column-start / grid-row-end/grid-column-end *
}
```

## Nivå 17

```css
#water-2 {
    grid-area: 2/3 / 5/-1;
}
```

## Nivå 18

```css
#poison {
    order: 5;
}
```

## Nivå 19

```css
.poison {
    order: -1;
}
```

## Nivå 20

```css
#garden {
    display: grid;
    grid-template-rows: 20% 20% 20% 20% 20%;
    grid-template-columns: 50%;
}
```

## Nivå 21

```css
#garden {
  display: grid;
  grid-template-rows: 20% 20% 20% 20% 20%;
  grid-template-columns: repeat(5, 12.5%);
}
```

## Nivå 22

```css
#garden {
    display: grid;
    grid-template-columns: 100px 3em 40%;
    grid-template-rows: 20% 20% 20% 20% 20%;
}
```

## Nivå 23

```css
#garden {
  display: grid;
  grid-template-rows: 20% 20% 20% 20% 20%;
  grid-template-columns: 1fr 5fr;
}
```

## Nivå 24

```css
#garden {
    display: grid;
    grid-template-rows: 20% 20% 20% 20% 20%;
    grid-template-columns: 50px 1fr 1fr 1fr 50px;
}
```

## Nivå 25

```css
#garden {
    display: grid;
    grid-template-rows: 100%;
    grid-template-columns: 75px 3fr 2fr;
}
```

## Nivå 26

```css
#garden {
    display: grid;
    grid-template-columns: 20% 20% 20% 20% 20%;
    grid-template-rows: 50px auto auto auto  1fr;
}
```

## Nivå 27

```css
#garden {
    display: grid;
    grid-template: 60% / 200px;
}
```

## Nivå 28

```css
#garden {
    display: grid;
    grid-template: 1fr 50px / 20% 80%;
}
```
