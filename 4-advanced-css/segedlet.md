# CSS - Cascade Style Sheet

## Ismétlés

- Oldal kinézetének formálására való
- Kulcs-érték párokból áll
- Végtelen opció, keressünk utána

```html
<link rel="stylesheet" type="text/css" href="assets/css/main.css"/>
```

## Animációk

Mint ahogy korábban felmerült, számtalan lehetőségre képes a CSS, melyek közé tartozik az animálás is. Ehhez először az animációt magát kell megadnunk.

Megadhatjuk, hogy miről-mire szeretnénk váltani:

```css
@keyframes my-animation {
    from {background-color: red;}
    to {background-color: yellow;}
}
```

Vagy százalékosan az egyes kulcslépéseket megadva:

```css
@keyframes my-animation {
    0%   {background-color: red;}
    25%  {background-color: yellow;}
    50%  {background-color: blue;}
    100% {background-color: green;}
}
```

Ezek után az adott elem CSS-ében kell alkalmazni az animációt:

```css
div {
    width: 100px;
    height: 100px;
    background-color: red;
    animation-name: my-animation;
    animation-duration: infinite;
}
```

## Media query-k

Idők során egyre több típusú, méretű és felbontású megjelenítő eszköz jelent meg, melyeken lehetséges az internet böngészése. Gondoljunk itt a nyomtatókra (nyomtatási nézet), laptopokra, telefonokra, tabletekre. Mindegyik különféle felbontással és mérettel rendelkezik, olyanokról nem is beszélve, mint a bevitel módja (touch/pointer), vagy kisegítő lehetőségek között az invertált színek.

Erre nyújtanak megoldást media query-k, ezeken keresztül lehetőség nyílik információt kérni az adott böngészőről, vagy készülékről. Egy-egy ilyen csoportba különféle CSS formázásokat állíthatunk be, melyek adott tulajdonság mellett érvényesülnek.

```css
@media screen and (min-width: 400px) {
  body {
    background-color: lightgreen;
  }
}

@media screen and (min-width: 800px) {
  body {
    background-color: lavender;
  }
}
```

Amennyiben nagyobb a projekt és mi magunk írjuk a teljes CSS-t, úgy jobb átláthatóságot biztosít, ha a html-ben a megfelelő media query szerint linkeljük a CSS-t.

```html
<link rel="stylesheet" media="screen and (min-width: 900px)" href="widescreen.css">
<link rel="stylesheet" media="screen and (max-width: 600px)" href="smallscreen.css">
```

## CSS Keretrendszerek

Látható, hogy a mai kornak megfelelve, egy-egy komplexebb oldal formázása rengeteg munkát igényel. Ezen felül általánosságban elmondható, hogy egészen sok esetben ugyanazok az elemek szükségesek egy-egy oldal felépítéséhez, csak egy-két apróságot módosítva. Szerencsére erre már elég korán rájöttek, ezért születtek meg a CSS keretrendszerek. Előnyük, hogy könnyen alkalmazhatóak, könnyen témázhatóak, általában jól átgondolt rendszerek és szükség esetén szerkeszthetőek, tovább bővíthetőek.

Gyakorlaton a [UIKit](https://getuikit.com/docs/introduction)-et használjuk. Többi keretrendszerhez hasonlóan, elég egy-egy class-t, illetve külön attribútumot megadni a formázáshoz.

Használatához az alábbi linkelések szükségesek, amennyiben letöltöttük és kitömörítettük a forrást:

```html
<head>
	<meta name="viewport" content="width=device-width, initial-scale=1">
    <link rel="stylesheet" href="css/uikit.min.css" />
    <script src="js/uikit.min.js"></script>
    <script src="js/uikit-icons.min.js"></script>
</head>
```

Illetve CDN-t használva:

```html
<head>
	<meta name="viewport" content="width=device-width, initial-scale=1">
	<link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/uikit/3.0.0-rc.17/css/uikit.min.css" />
	<script src="https://cdnjs.cloudflare.com/ajax/libs/uikit/3.0.0-rc.17/js/uikit.min.js"></script>
	<script src="https://cdnjs.cloudflare.com/ajax/libs/uikit/3.0.0-rc.17/js/uikit-icons.min.js"></script>
</head>
```

Pár példa az eszköztárából:

```html
<body class="uk-height-viewport">
    <div class="uk-container">	<!-- This will be aligned center -->
        <h1>My awesome site!</h1>
        
        <ul class="uk-list uk-list-striped">
            <li>Very</li>
            <li>important</li>
            <li>things!</li>
        </ul>

		<input type="button" value="Click me!" class="uk-button uk-button-secondary"/>

        <div class="uk-clearfix">
            <div class="uk-float-right">
                <div class="uk-card uk-card-default uk-card-body">It floats right</div>
            </div>
            <div class="uk-float-left">
                <div class="uk-card uk-card-default uk-card-body">It floats left</div>
            </div>
        </div>

        <div uk-grid>
            <div class="uk-width-1-2"></div>
            <div class="uk-width-2-5"></div>
        </div>

    </div>
</body>
```





## További információk

- https://github.com/kir-dev/heller-tanfolyam/blob/master/3-css/segedlet.md
- https://www.w3schools.com/css/css3_animations.asp
- https://developer.mozilla.org/en-US/docs/Web/CSS/CSS_Animations/Using_CSS_animations
- https://www.w3schools.com/cssref/css3_pr_mediaquery.asp
- https://developer.mozilla.org/en-US/docs/Web/CSS/Media_Queries/Using_media_queries
- https://getuikit.com/docs/introduction
- https://github.com/dons20/UIKit-VSCode