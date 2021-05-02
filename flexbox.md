# Flexbox

---

# Introduktion

--

```html
<div class="parent">
  <div class="child child__one">1</div>
  <div class="child child__two">2</div>
  <div class="child child__three">3</div>
  <div class="child child__four">4</div>
</div>
```

--

```css
.parent {
  border: 0.5rem solid #192a56;
}

.child {
  color: #fff;
  font-family: sans-serif;
  font-size: 2rem;
  padding: 1rem;
}

.child__one {
  background-color: #1abc9c;
}

.child__two {
  background-color:#3498db;
}

.child__three {
  background-color: #8e44ad;
}

.child__four {
  background-color: #e67e22;
}
```

--

Bild på resultat in här

---

# Aktivera flexbox

--

```css
.parent {
  /* Övrig CSS ej med i exemplet */
  display: flex;
}
```

--

Bild på resultat in här

---

# Container och items

--

## Flex container

--

## Flex items

---

# P: flex-direction

--

## row

```css
.parent {
  border: 0.5rem solid #192a56;
  
  display: flex;
  flex-direction: row; /* Standardvärdet för flex */
}
```

BILD

--

## row-reverse

```css
.parent {
  border: 0.5rem solid #192a56;

  display: flex;
  flex-direction: row-reverse;
}
```

BILD

--

## column

```css
.parent {
  border: 0.5rem solid #192a56;

  display: flex;
  flex-direction: column;
}
```

BILD

--

## column-reverse

```css
.parent {
  border: 0.5rem solid #192a56;

  display: flex;
  flex-direction: column-reverse;
}
```

BILD

---

# P: justify-content

--

## flex-start

```css
.parent {
  border: 0.5rem solid #192a56;

  display: flex;
  justify-content: flex-start; /* Standardvärdet */
}
```

BILD

--

## flex-end

```css
.parent {
  border: 0.5rem solid #192a56;

  display: flex;
  justify-content: flex-end;
}
```

BILD

--

## center

```css
.parent {
  border: 0.5rem solid #192a56;

  display: flex;
  justify-content: center;
}
```

BILD

--

## space-between

```css
.parent {
  border: 0.5rem solid #192a56;

  display: flex;
  justify-content: space-between;
}
```

BILD

--

## space-around

```css
.parent {
  border: 0.5rem solid #192a56;

  display: flex;
  justify-content: space-around;
}
```

BILD

--

## space-evenly

```css
.parent {
  border: 0.5rem solid #192a56;

  display: flex;
  justify-content: space-evenly;
}
```

BILD

---

# P: align-items

--

## stretch

```css
.parent {
  border: 0.5rem solid #192a56;
  
  display: flex;
  align-items: stretch; /* Standardvärdet */
}
```

BILD

--

## flex-start

```css
.parent {
  border: 0.5rem solid #192a56;

  display: flex;
  align-items: flex-start;
}
```

BILD

--

## flex-end

```css
.parent {
  border: 0.5rem solid #192a56;

  display: flex;
  align-items: flex-end;
}
```

BILD

--

## center

```css
.parent {
  border: 0.5rem solid #192a56;

  display: flex;
  align-items: center;
}
```

BILD

--

## baseline

```css
.parent {
  border: 0.5rem solid #192a56;

  display: flex;
  align-items: baseline;
}
```

BILD

---

# P: flex-wrap

--

## nowrap

```css
.parent {
  border: 0.5rem solid #192a56;

  display: flex;
  flex-wrap: nowrap; /* Standardvärdet */
}
```

BILD

--

## wrap

```css
.parent {
  border: 0.5rem solid #192a56;

  display: flex;
  flex-wrap: wrap;
}
```

BILD

--

## wrap-reverse

```css
.parent {
  border: 0.5rem solid #192a56;

  display: flex;
  flex-wrap: wrap-reverse;
}
```

BILD

---

# P: flex-flow

--

## flex-direction flex-wrap

Doh!

--

## row nowrap

```css
.parent {
  border: 0.5rem solid #192a56;

  display: flex;
  flex-flow: row nowrap; /* Standardvärdet */
}
```

BILD

--

## Ex 1


```css
.parent {
  border: 0.5rem solid #192a56;

  display: flex;
  flex-flow: 
}
```

BILD

--

## Ex 2


```css
.parent {
  border: 0.5rem solid #192a56;

  display: flex;
  flex-flow: 
}
```

BILD

---

# P: align-content OBS RUTAN HEY!

--

## Information

Doh!

--

## normal

```css
.parent {
  border: 0.5rem solid #192a56;

  display: flex;
  align-content: normal; /* Standardvärdet */
}
```

BILD

--

## flex-start

```css
.parent {
  border: 0.5rem solid #192a56;

  display: flex;
  align-content: flex-start; 
}
```

BILD

--

## flex-end

```css
.parent {
  border: 0.5rem solid #192a56;

  display: flex;
  align-content: flex-end; 
}
```

BILD

--

## center

```css
.parent {
  border: 0.5rem solid #192a56;

  display: flex;
  align-content: center; 
}
```

BILD

--

## stretch

```css
.parent {
  border: 0.5rem solid #192a56;

  display: flex;
  align-content: center; 
}
```

BILD

--

## space-between

```css
.parent {
  border: 0.5rem solid #192a56;

  display: flex;
  align-content: space-between; 
}
```

BILD

--

## space-around

```css
.parent {
  border: 0.5rem solid #192a56;

  display: flex;
  align-content: space-around; 
}
```

BILD

---

# C: order

--

## Parent

```css
.parent {
    border: 0.5rem solid #192a56;

    display: flex;
}
```

--

## Ex 1

Doh!

BILD

--

## Ex 2

Doh!

BILD

---

# C: flex

--

## Parent

```css
.parent {
    border: 0.5rem solid #192a56;

    display: flex;
}
```

--


---

# C: flex-grow

--

## Parent

```css
.parent {
    border: 0.5rem solid #192a56;

    display: flex;
}
```

--


---

# C: flex-shrink

--

## Parent

```css
.parent {
    border: 0.5rem solid #192a56;

    display: flex;
}
```

--


---

# C: flex-basis

--

## Parent

```css
.parent {
    border: 0.5rem solid #192a56;

    display: flex;
}
```

--


---

# C: align-self

--

## Parent

```css
.parent {
    border: 0.5rem solid #192a56;

    display: flex;
}
```

--

