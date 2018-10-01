

## CSS - Cascading Style Sheet
------

Eddig a weboldalunk stuktúráját írtuk le, a következőkben pedig a megformázásával fogunk foglalatoskodni. A CSS lehet külön fájlba írni, vagy pedig az oldal `<head>` részében egy nyitott `<style type="text/css"></style>` tagek közé is írhatjuk. Ha külön fájlba írjuk akkor azt szintén az oldal `<head>` részében linkelnünk kell. Ezt a következő kód beillesztésével tehetjük meg:

~~~html
<link rel="stylesheet" type="text/css" href="assets/css/main.css"/>
~~~

A fájl elérés utját a már ismert `href` attribútumban adhatjuk meg.

#### A dokumentum elemeinek az elérése

A dokumentum elemeit három féle képpen tudjuk elérni.

* magán a tag nevén, de ez befolyásolja az összes ilyen nevű elemet
* egy (egyedi) azonosítón keresztül, amit attributumként megadhatunk, `id`
* css osztályokon keresztül, amit ha szeretnénk több elemere is definiálhatunk `class`

Példa mindhárom módszerre:

~~~html
<head>
    <style type="text/css">
    
    /*a tag nevén keresztül*/
    p {
        color: red;
    }

    /*id-n keresztül*/
    #header {
        color: red;
    }

    /*class-on keresztül*/
    .post {
        color: red;
    }

    </style>
</head>
<body>
    <p> bekezdés </p>
    <p> bekezdés </p>

    <div id="header">
        az oldal headerje lesz majd
    </div>

    <div class="post">
        egy post az oldalon
    </div>

    <div class="post">
        egy másik post az oldalon
    </div>
</body>
~~~

Innentől kezdve, hogy elérjük a html dokumentumunk elemeit a kapcsos zárójelben megadott tulajdonságok érvényesek lesznek az adott elemre. Több kategóriába soroljuk a stílusokat, a következőkben ezeket fogjuk kifejteni.

#### Színkezelés

A színeket meg lehet adni hexadecimális formában melynek van egy rövidített formája is, az rgb() és az rgba() függvények segítségével amiből a második segítségével tudjuk az átlátszóságot is szabályozni. Továbbá megadhatjuk a szín angol nevével is.

* #FF00AA - #FFFFFF
* #F0A - #FFF
* rgb(0, 125, 255)
* rgba(0, 125, 255, 0.5)
* white, black, blue, red ...

#### A Szövegformázió stílusok

~~~css
color: #000000; /*a betűk színe, hexadecimálisan, rgb(), rgba(), szín-neve-angolul*/
font-family: Arial, Helvetica; /*a betű típusa (font-face)*/
font-size: 15px; /*a betű mérete*/
font-weight: 400; /*a betű vastagsága 100-tól, 900-ig hasonló a boldhoz*/
font-style: italic; /*a betű stílusa, bold*/
letter-spacing: 15px; /*betűköz*/
line-height: 15px; /*sorköz*/
text-align: center; /*szöveg kizárása, left, right, center, justify*/
text-decoration: underline; /*szöveg dekorálása*/
text-shadow: 0px 1px 2px #000000; /*árnyék, left, top, blur, color*/
text-transform: uppercase; /*csupa nagy betű, kis betű, kapitalizált stb.*/
~~~

#### Háttér és keret formázások

~~~css
background-attachment: fixed; /*görgethető legyen a háttér vagy ne*/
background-color: red; /*háttér színe*/
background-image: url(‘images/pic.png’); /*háttérkép*/
background-position: left top; /*a háttér pozicioja*/
background-repeat: no-repeat; /*a hatter ismetlese*/
background: transparent url(‘../images/pic_holder.png’) top left norepeat; /*itt megadhatjuk mindezt egyszerre is*/
border-width: 2px; /*border vastagsága*/
border-color: #234f8a; /*border színe*/
border-style: solid; /*stílusa*/
border: 3px solid dashed; /*megadható egyszerre itt is*/
border-top: 3px solid dashed; /*csak felső margó az elemre left, right, bottom is lehetséges*/
border-radius: 2px; /*a sarkok lekerekítése bizonyos sugárral*/
box-shadow: 0px 3px 4px #000000; /*árnyéka az elemnek*/
~~~

#### CSS selectorok és pszeudo osztályok

A selectorok segítségével speciálisan is tudunk html elemeket kiválasztani (fontos, hogy a kiértékelés jobbról balra halad).

* div, p - kijelöli a div és a p elemeket
* div p - kijelöli azokat a p elemeket, amik egy div-ben vannak (gyerek viszony)
* div > p - kijelöli azokat a p elemeket, aminek közvetlen szülője egy div (szülő viszony)
* div + p - kijelöli azokat a p elemeket, amelyek közvetlenül egy div után következnek (testvér viszony)
* div ~ p - kijelöli azokat a p elemeket, amelyek egy div után következnek

A pszeudo osztályok segítségével, pedig speciálisan tudunk egy elemre stílusokat definiálni, például amikor az egér az adott elem felett van. Néhány pszeudo osztály:

* :link, :visited, :active
* :hover
* :first-child, :last-child
* :before, :after

#### Hasznos információk
A web világban a folyamatos fejlődés miatt, a gyors és hatékony fejlesztés érdekében fontos, hogy használjuk a keresőket.

### Hasznos linkek
https://www.w3schools.com/css/css3_flexbox.asp
https://www.w3schools.com/css/css_grid.asp
https://caniuse.com/
https://developer.mozilla.org/en-US/docs/Web/

