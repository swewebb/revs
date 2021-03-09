# Python - Kapitel 10

---

# Importera random

--

```python
import random
```

```python
from random import randint
```

Vi använder slumptal i Python genom att importera modulen **random**

---

# random()

--

Ger ett flyttal i intervallet 0,..,1.0. 

Blir aldrig exakt 0 eller 1.

--

```python
import random

r = random.random()
print(r)

0.33244833625067194
```

--

```python
from random import random

r = random()
print(r)

0.14875270475440316
```

---

# randrange()

--

Ger ett slumptal (heltal) i motsvarande range

--

```python
# 1-10 heltal
from random import randrange

r = randrange(1, 10 + 1)
print(r)

3
```

--

```python
# 1-10 udda heltal
from random import randrange

r = randrange(1, 10, 2)
print(r)

9
```

--

```python
# 1-10 udda heltal
from random import randrange

for i in range(10):
    r = randrange(1, 10, 2)
    print(r, end=" ")

9 7 9 7 9 3 7 3 7 1
```

--

```python
# 0-10 jämna heltal
from random import randrange

r = randrange(0, 10, 2)
print(r)

4
```

--

```python
# 0-10 jämna heltal
from random import randrange

for i in range(10):
    r = randrange(0, 10, 2)
    print(r, end=" ")

2 0 8 4 6 8 8 0 4 2 
```

--

```python
# 0-10 jämna heltal
from random import randrange

r = ', '.join([str(randrange(0, 10, 2)) for i in range(10)])
print(r)

8, 0, 0, 2, 4, 0, 0, 4, 4, 4
```

---

# randint()

--

Ger ett heltal mellan a och b. Utdatan kan verkligen anta extremvärdet.

--

```python
# 1-10 heltal = alias till randrange(a, b+1)
from random import randint

r = randint(1, 10)
print(r)

10
```

---

# choice()

--

Väljer slumpmässigt ett element ur en sekvens, t.ex. en sträng, lista, tippel eller en range

--

```python
# Väljer ett slumpmässigt element ur en sekvens
from random import choice

text = "ABCDE"
r = choice(text)

print(r)

B
```

--

```python
# Väljer ett slumpmässigt element ur en sekvens
from random import choice

lista = ['Kalle', 'Ada', 'Humle', 'Dumle']
r = choice(lista)

print(r)

Ada
```

--

```python
# Väljer ett slumpmässigt element ur en sekvens
from random import choice

tupel = 'Kalle', 'Ada', 'Humle', 'Dumle'
r = choice(tupel)

print(r)

Dumle
```

--

```python
# Väljer ett slumpmässigt element ur en sekvens
from random import choice

numbers = range(50, 60 +1)
r = choice(numbers)

print(r)

57
```

---

# shuffle()

--

Blandar sekvensen x på plats. Extra parameterna kan vara en slumptalsfunktion (default är random()).

--

```python
x
```

---

# sample()

--

Drar slumpmässigt _k_ st element ur en population.

--

```python
x
```

---

# getstate() och setstate()

--

Läs av och sätt generatorns "tillstånd" för att kunna återupprepa en viss slumptalsföljd

--

```python
x
```

---
