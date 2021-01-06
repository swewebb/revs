# linux-05

---

# Filsystemet

---

# Hemkatalog

--

Alla användare i systemet har en egen hemkatalog.

Återfinns i **/home**,t.ex **/home/pelle**

Det är här vi hamnar när vi loggar in.

Förkortas **~**

Din användare äger allt i katalogen.

---

# Absoluta- och relativa sökvägar

--

**Absolut sökväg** = utgår från rooten, t.ex `cd /home/pelle`

--

**Relativ sökväg** = utgår mappen man står i, t.ex `cd pelle`

---

# Navigera

--

`cd` = Change Directory

--

`cd /etc/apt/`

Förflyttar dig till katalogen **/etc/apt** oavsett var i filträdet du befinner dig.

--

`cd /`

Förflyttar dig till roten på filträdet oavsett var i filträdet du befinner dig.

`cd ~` eller `cd`

Förflyttar dig till din hemkatalog (t.ex **/home/pelle**) oavsett var i filträdet du befinner dig.

--

`cd ..`

Förflyttar dig ett steg bakåt/uppåt i filträdet, t.ex från **/home/pelle** till **/home/**

--

`cd ../..`

Förflyttar dig ett steg bakåt/uppåt i filträdet, t.ex från **/home/pelle** till **/**

--

`cd musik`

Förflyttar dig in i katalogen **musik**, som återfinns i katalogen där du befinner dig.

---

# Lista

--

`ls` = List ("ell-ess")

--

## Enkel listning

`ls`

![linux05-01](images/linux-05-01.png)

Vit = fil, blå = katalog, turkos = mjuk länk

--

## Lista i långt format

`ls -l`

![linux05-02](images/linux-05-02.png)


--

## Lista dolda filer/kataloger

`ls -a`

![linux05-03](images/linux-05-03.png)

`ls -A`

![linux05-04](images/linux-05-04.png)

--

# Kombinera

`ls -Al`

![linux05-05](images/linux-05-05.png)

---

# Se vart man är

--

`pwd`

![linux05-06](images/linux-05-06.png)

---

# Se innehållet i en fil

--

`cat` = concatenate files and print on the standardoutput

--

![linux05-06](images/linux-05-07.png)

--

![linux05-09](images/linux-05-09.png)

---

## Långt innehåll

--

`more`

**Enter** = hoppa fram en rad.

**Mellanslag** = hoppa fram en sida

--

`ls /etc | more` eller t.ex `more dump`

--

`less`

Med `less` kan duanvända upp/ned-pil för att förflytta dig i utdatat.

---

# Skapa filer

--

`touch`

--

`touch kaka` = Skapar en tom fil med namnet kaka

![linux05-09](images/linux-05-10.png)

--

`touch anka1 anka2 anka3` = Skapar tre tomma filer

![linux05-11](images/linux-05-11.png)

--

`touch --date="2020-12-24 15:00:00" anka1`

![linux05-12](images/linux-05-12.png)

![linux05-13](images/linux-05-13.png)


--

`cat >`, avsluta med `CTRL + D`

![linux05-08](images/linux-05-08.png)

---

# Information om en fil

--

`stat` = Display file or file system status

--

![linux05-14](images/linux-05-14.png)

Här kan vi bland annat se när filen senast öppnades eller modifierades.

---

# Skapa kataloger

--

Doh!

---

# Ta bort filer

--

Doh!

---

# Ta bort kataloger

--

Doh!

---

# Kopiera

--

Doh!

---

## Filer

--

Doh!

---

## Kataloger

--

Doh!

---

# Döpa om filer/kataloger

--

Doh!

---

# Länkar

--

Doh!

--

## Mjuka länkar

Doh!

--

## Hårda länkar

stat:a

---

# Allting är filer (eller processer)

--

Doh!

---

# Visa monterade lagringsenheter

--

Doh!

---

# Slut!