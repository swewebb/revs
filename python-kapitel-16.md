# Python - Kapitel 16

---

# Repetition om listor m.m.

--

```python
string = 'abcdefghijklmnop'
x = string[1:4+1]
print(x)
```

```
bcde
```

--

```python
string = 'abcdefghijklmnop'
x = string.split('d')
print(x)
```

```python
['abc', 'efghijklmnop']
```

--

```python
string = 'abcdefghijklmnop'
lista = list(string)
print(lista)
```

```python
['a', 'b', 'c', 'd', 'e', 'f', 'g', 'h', 'i', 'j', 'k', 'l', 'm', 'n', 'o', 'p']
```

--

```python
lista = list(string)
x = lista[1:4+1]
print(x)
```

```python
['b', 'c', 'd', 'e']
```

--

```python
lista = list(string)
x = '-'.join(lista)
print(x)
```

```python
a-b-c-d-e-f-g-h-i-j-k-l-m-n-o-p
```

--

```python
print('-'.join(list('abcdefghijklmnop')))
```

```python
a-b-c-d-e-f-g-h-i-j-k-l-m-n-o-p
```

--

```python
string = 'abcdefghijklmnop'
lista = list(string)
tippel = tuple(string)

print(lista, end='\n\n')
print(tippel)
```

```python
['a', 'b', 'c', 'd', 'e', 'f', 'g', 'h', 'i', 'j', 'k', 'l', 'm', 'n', 'o', 'p']

('a', 'b', 'c', 'd', 'e', 'f', 'g', 'h', 'i', 'j', 'k', 'l', 'm', 'n', 'o', 'p')
```

---

# Sammanfattning av listmetoder och listfunktioner

--

## len(lista)

--

Längden av listan. Sista index är `len(lista)-1`

```python
lista = ['A', 'B', 'C', 'D']
x = len(lista)
y = len(lista)-1

print(x, y)
```

```python
4 3
```

--

## sorted(lista)

--

Returnerar en sorterad lista, där elementen måste vara av samma typ

```python
lista = ['X', 'B', 'E', 'D']
x = sorted(lista)
print(x)
```

```python
print(sorted(['X', 'B', 'E', 'D']))
```

```python
['B', 'D', 'E', 'X']
```

--

## lista.append(x)

--

Lägger till elementet **x** i slutet av listan

```python
lista = ['A', 'B', 'C', 'D']
lista.append('X')
print(lista)
```

```python
['A', 'B', 'C', 'D', 'X']
```

--

## lista.extend(lista2)

--

Förlänger listan med en annan lista

```python
lista1 = ['A', 'B', 'C', 'D']
lista2 = [1, 2, 3]
lista1.extend(lista2)
print(lista1)
```

```python
['A', 'B', 'C', 'D', 1, 2, 3]
```

--

## lista.insert(i,x)

--

Infogar elementet **x** på plats **i**.

```python
lista = ['A', 'B', 'C', 'D']
lista.insert(2, 'X')
print(lista)
```

```python
['A', 'B', 'X', 'C', 'D']
```

--

## lista.remove(x)

--

Tar bort första elementet med värdet **x**

```python
lista = ['A', 'B', 'C', 'D', 'C']
lista.remove('C')
print(lista) 
```

```python
['A', 'B', 'D', 'C']
```

--

## lista.pop(i)

--

Tar bort elementet med index **i** och returnerar värdet. Om **i** utelämnas är standard (default) att sista värdet tas bort.

```python
lista = ['A', 'B', 'C', 'D']
lista.pop()
lista.pop(1)
print(lista) 
```

```python
['A', 'C']
```

--

## lista.index(x)

--

Returnerar index för första förekomst av element **x**.

```python
lista = ['A', 'B', 'C', 'D', 'C', 'C']
x = lista.index('C')
print(x)
```

```python
2
```

--

## lista.count(x)

--

Returnerar antalet element med värdet **x**.

```python
lista = ['A', 'B', 'C', 'D', 'C']
x = lista.count('C')
print(x)
```

```python
2
```

--

## lista.sort()

--

Sorterar listan på plats

```python
lista = ['E', 'B', 'A', 'D', 'C']
lista.sort()
print(lista)
```

```python
['A', 'B', 'C', 'D', 'E']
```

--

## lista.reverse()

--

Vänder på ordningen av elementen i listan.

```python
lista = ['A', 'B', 'C', 'D']
lista.reverse()
print(lista)
```

```python
['D', 'C', 'B', 'A']
```

---

# Enumerate

--

Ibland vill man loopa över en sträng/lista/tippel så att man har tillgång till både index och listelementet samtidigt, och då kan man använda `enumerate`.

--

```python
txt = 'Teknik'

for index, char in enumerate(txt):
    print(index, char)
```

```python
0 T
1 e
2 k
3 n
4 i
5 k
```

--

```python
tippel = tuple('Teknik')
print(tippel)
for index, char in enumerate(tippel):
    print(index, char)
```

```python
('T', 'e', 'k', 'n', 'i', 'k')
0 T
1 e
2 k
3 n
4 i
5 k
```

---

# Dictionaries

## _Associativ array_

## _Ordböcker_

--

Förutom vanliga strängar, tipplar och listor finns i Python en datatyp som kallas för "associativ array", eller en "dictionary".

Denna datatyp fungerar ungefär som en lista, men istället för heltalsindex används ett namn på varje element, en s.k. **key**, vanligtvis en sträng, men det kan vara ett tal också.

--

Ett dictionary består av en mängd par där första delen kallas för **nyckel** och andra delen för **värde**. 

Varje par av nyckel-värde kallas för en **post** eller **item**.

--

Istället för hakparenteser används "måsvingar" { } och kolon när dictionariet definieras, men hakparenteser används så snart vi gör indexeringar i det:

```python
dict = { nyckel_1:värde_1, nyckel_2:värde_2, nyckel_3:värde_3, … , nyckel_n:värde_n }

print(dict[nyckel_i]) # Skriver ut värde_i
```

--

Dictionaries är uppbyggd med hashkodning för snabbhet, och därför sparas inte elementen alltid i den ordning vi skrev dem och är inte heller sorterade på nyckelvärdena.

--

Nya värden läggs till och gamla värden ändras genom att ange en (ny) nyckel och ett nytt värde:

```python
dict[ny_nyckel] = nytt_varde
```

--

Värde i tas bort med...

```python
del(dict[nyckel_i])
```

---

# Exempel 1

--

Doh!

---

# Exempel 2

--

Doh!

---

# Exempel 3

--

Doh!

---

# Exempel 4

--

Doh!

---
