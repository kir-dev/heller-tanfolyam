## Mi a JavaScript?
A JavaScript programozási nyelv egy szkriptnyelv, amelyet weboldalakon elterjedten használnak. A JavaScript a klien értelmezi, a futási környezet jellemzően egy webböngésző JavaScript-motorja.

A JavaScript és a Java két különböző nyelv!

## JavaScript beágyazása

A JavaScript kódot közvetlenül a HTML oldalunkba ágyazzuk be ```<script>``` tag-ek közé.
```html
  <script>  
    alert("Helló Világ!");
  </script>
```

Lehetőségünk van külön file-ba megírni a JavaScript kódunkat. Érdemes ezt használni, hiszen így egy átláthatóbb alkalmazást kaphatunk. Ilyenkor a ```<script>``` tag ```src``` attributumába kell a file elérési útvonalát megadnunk.
```html
<script src="myscripts.js"></script>
```

## Változó
A JavaScript nyelvben változókat deklarálhatunk. A változókban értékeket tárolhatunk, melyeken műveleteket tudunk végrehajtani.
```javascript
var a = 2;
var b = 2;
var sum = a + b;
var tomb = [1,2,3];
```
++++++++++++++++++++++

## Operátorok
### Aritmetikai operátorok
**Összeadás (+)**

```javascript
x = 1 + 1;  // = 2
```

**Kivonás (-)**

```javascript
x = 1 - 1;  // = 0
```

**Szorzás (*)**

```javascript
x = 5 * 5;  // = 25
```

**Osztás (/)**

```javascript
x = 25 / 5;  // = 5
```

**Maradékos osztás (%)**

```javascript
x = 28 % 5;  // = 3
```

### Logikai operátorok
- logikai és: a && b
- logikai vagy: a || b
- tagadás: !a
- Kisebb mint: <
- Nagyobb mint: >
- Kisebb egyenlő: <=
- Nagyobb egyenlő: >=
- Egyenlő: ==
- Nem egyenlő: !=
- Teljesen egyenlő (típus is): ===
- Nem teljesen egyenlő (típust is vizsgál): !==


## Szelekció
Feladatok közötti választás. Vagy az igaz, vagy a hamis ág le fog futni.

```javascript
var a = 5;
if(a == 7) { // Feltételem
  // Igaz
  console.log("A értéke 5");
} else {
  // Hamis
  console.log("A értéke nem 5");
}
```
A hamis ág elhagyható.

```javascript
var a = 5;
if(a == 7) { // Feltételem
  // Igaz
  console.log("A értéke 5");
}
```
## Ciklus
```
for (intiializer; condition; modifier) {

}
```
- Initializer: itt egy ciklus változóban megadunk egy értéket, hogy honnan induljon a számlálás. Általában ezt a ciklus változót “i”-nek szokták nevezni, de igazából bárhogy elneveztheted.
- Condition: ide jön a feltétel, amely igaz/hamis értékre lesz letesztelve minden egyes lefutásnál.
- Modifier: ide jön egy parancs ami módosítja a feltétel értékét, amely így egy idő után hamis lesz.
A fent felsorolt paramétereket pontosvesszővel választjuk el.

Egy nagyon egyszerű példában számoljunk el 0-tól 10-ig és ezt írassuk ki a konzolban. Ehhez az alábbi kódra lesz szükség:
```
for (var i = 0; i < 10; i++) {
	console.log(i);
}
```

## Események
Webfejelsztés során a kódjaink nagyrésze valamilyen esemény hatására futnak le.

```html
  <button value="Kattints rám!" onClick="alert('Hello!')">
```
A fenti kódrészlet a gomb click eseményére egy felugró ablakot jelenít meg. A click eseményen kívűl rengteg esemény létezik, amiket használhatunk.
|                  |                                                  |
| ---------------- | ------------------------------------------------ |
| **Esemény neve** | **Az esemény mikor következik be**               |
| onAbort          | A felhasználó megszakítja a kép betöltését       |
| onBlur           | Az egérrel az aktuális mezon kívülre kattint     |
| onChange         | Megváltoztatunk egy űrlapbeli értéket            |
| onClick          | Űrlap elemre vagy linkre kattint                 |
| onDblClick       | Űrlap elemre vagy linkre duplán kattint          |
| onDragDrop       |                                                  |
| onError          | Ha kép vagy dokumentum betöltésekor hiba lép fel |
| onFocus          | Kijelöli az űrlap egy elemét                     |
| onKeyDown        |                                                  |
| onKeyPress       |                                                  |
| onKeyUp          |                                                  |
| onLoad           | A böngésző új oldalt tölt be                     |
| onMouseDown      |                                                  |
| onMouseMove      |                                                  |
| onMouseOut       | Az egér lekerül a linkről                        |
| onMouseOver      | Az egér a link felé kerül                        |
| onMouseUp        |                                                  |
| onMove           |                                                  |
| onReset          | Űrlap törlésekor                                 |
| onResize         |                                                  |
| onSelect         | Új mezőt jelöl ki                                |
| onSubmit         | Űrlap elküldésekor                               |
| onUnload         | Másik HTML oldalra lép                           |
## Függvények
A JavaScript-ben is rendkívül fontos szerepet kapnak a függvények. A nyelv számos függvényt tartalmaz, például az előző pontban megismert alert() függvény is ezek közül való.

```javascript
function osszead(x, y){
  return x + y;
}

console.log(osszead(1, 1));

```
A zárójel között megadott értkékek a függvény paraméterei, a return utáni pedig a visszatérési értéke. Ezeknek a megadása nem kötelező.

```javascript
function hello(){
  console.log("Szia");
}

hello();
```

## DOM manipuláció
JavaScript-tel legtöbbször a weboldal valamely részét manipuláljuk valamilyen esemény hatására. 
Az alábbi kódrészlet az demo ID-val rendelkező elembe írja be a 'Hello' stringet.

```html
<p id="demo"></p>

<script>
   document.getElementById("demo").innerHTML = "Hello"; 
</script>
```


