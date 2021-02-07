# Python - Kapitel 9

---

# Introduktion

--

<span class="fragment">Hittills har vi skrivit all kod från scratch varje gång, men en bra programmerare
strukturerar upp sin kod för att få bitar som är återanvändbara</span>

<span class="fragment">Dessa återanvändbara kodsnuttar kallas för <b>funktioner</b></span>

<span class="fragment">Vi har redan använt oss av funktioner, t.ex. `len()`, `print()`, `int()`,
`range()`, osv.</span>

<span class="fragment">Nu ska vi göra egna funktioner</span>

--

# Exempel på en funktion

```python
# Exempel på en funktion med två parametrar
def skriv_summa(x, y):
    summa = x + y
    print('Summan är:', summa)

# Huvudprogram
a = 3
b = 4
skriv_summa(a, b)
```
--

En funktion skapas genom att man definierar den med **namn**, **parametrar** inom parentes, och **kolon**.

Det följande programblocket (indenterat precis som vanligt efter ett kolon) tillhör funktionen.

Sedan skriver vi vårt huvudprogram precis som vanligt, och anropar där vår nya funktion med argument.

## Vad händer i anropet?

Parametrarna **x**, **y** och variabeln **summa** är lokala i funktionen och kan inte ses utanför funktionen.

Värdet av argumenten i funktionsanropet kopieras till parametrarna.

Funktionen exekveras.

När anropet avslutats fortsätter programmet efter funktionsanropet.

---

# Defaultvärden på parametrarna

```python
# Exempel på en funktion med två parametrar
def skriv_summa(x, y = 1):
    summa = x + y
    print('Summan är:', summa)

# Huvudprogram
a = 3
b = 4

skriv_summa(a, b)
skriv_summa(b)
```

--

Det finns ibland anledning att utlämna vissa parametrar som oftast antar ett specifikt värde.

Den möjligheten kan man ange i parameterlistan genom att sätta ett visst default-värde på en parameter.

De parametrar som kan ha default-värde måste ligga längst till höger i listan, annars vet inte Pyhton vilken man har angett och vilka som ska få default-värden.

---

# Funktioner som returnerar värden

--

```python
# Exempel på en funktion som returnerar ett värde
def medelvarde(x, y):
    medel = (x + y ) / 2
    return medel

# Huvudprogram
a = 3
b = 4
m = medelvarde(a, b)

print('Medelvärdet är:', m)
```

--

Väldigt vanligt är att vi vill ha tillbaka något från funktionsanropet, dvs att det skall returnera något värde.

Detta gör vi med **return**, och värdet "förs över" till utanför funktionsanropet och sparas lokalt.

--

```python
# Exempel på en funktion som returnerar ett värde
def medelvarde(x, y):
    """Returnerar medelvärdet av parametrarna x och y"""
    medel = (x + y ) / 2
    return medel

# Huvudprogram
a = 3
b = 4
m = medelvarde(a, b)

#print('Medelvärdet är:', m)

help(medelvarde)
```

--


```html
medelvarde(x, y)
    Returnerar medelvõrdet av parametrarna x och y
```

--

```python
# Exempel på en funktion som returnerar ett värde
def medelvarde(x, y):
    """Returnerar medelvärdet av parametrarna x och y"""
    return (x + y ) / 2

# Huvudprogram
a = 3
b = 4
m = medelvarde(a, b)

print('Medelvärdet är:', m)
```

---

# Mer om globalt och lokalt

--

Argumentvärden som skickas in till funktioner kopieras till minnesstacken och är synliga endast inne i funktionerna.

När funktionen avslutas frigörs minnet.

Variabler som definieras utanför alla funktioner är dock globala, och syns överallt så länge ingen lokal variabel har samma namn och "skymmer sikten".

--

```python
b = 6

def leppard():
    b = 10
    print(b)

print(b)
leppard()
print(b)
```

```python
6
10
6
```

--

```python
b = 6

def leppard():
    global b
    b = 10
    print(b)

print(b)
leppard()
print(b)
```

```python
6
10
10
```

Vill man tilldela en global variabel inne i en funktion måste man deklarera den som **global**.

---

# Import av moduler

--

Python distribueras med en stor mängd färdigskrivna funktioner och definierade konstanter.

Dessa finns samlade i moduler som kan läggas till efter eget behag med hjälp av instruktionen `import`.

Exempelvis ligger en massa matematiska funktioner och konstanter i modulen **math.py**.

Vid importen skriver man dock endast `import math`.

Vid användning skriver man **modulnamn.funktionsnamn**.

--

```python
import math

pi = math.pi
sq = math.sqrt(2)
sin = math.sin(math.pi / 2)

print(pi, sq, sin)
```

--

```python
from math import *

pi = pi
sq = sqrt(2)
sin = sin(pi / 2)

print(pi, sq, sin)
```

--

```python
from math import pi, sqrt, sin

pi = pi
sq = sqrt(2)
sin = sin(pi / 2)

print(pi, sq, sin)
```

--

```python
import math

for method in dir(math):
    print(method)
```

```python
__doc__ __loader__ __name__ __package__ __spec__ acos acosh asin asinh atan atan2 atanh ceil comb copysign cos cosh degrees dist e erf erfc exp expm1 fabs factorial floor fmod frexp fsum gamma gcd hypot inf isclose isfinite isinf isnan isqrt ldexp lgamma log log10 log1p log2 modf nan perm pi pow prod radians remainder sin sinh sqrt tan tanh tau trunc 
```

--

```python
import math

help(math)
```

```python
NAME
    math

DESCRIPTION
    This module provides access to the mathematical functions
    defined by the C standard.

FUNCTIONS
    acos(x, /)
        Return the arc cosine (measured in radians) of x.
    
    acosh(x, /)
        Return the inverse hyperbolic cosine of x.
```

---

# SLUT

---