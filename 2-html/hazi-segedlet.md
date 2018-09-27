# Házi feladat segédlet 

Ahogy az előadáson elhangzott, a HTML egymásba ágyazott tag-ekből épül fel. Az alábbi kód az előadáson bemutatott oldal kezdőlapját írja le.

```jade
header.header
  div.container
    h1.logo Your logo
nav.nav
  div.container
    ul
      li
        a Hírek
      li
        a Rólam
      li
        a Kapcsolat
div.container
  section.content
    article.post
      header.post-header
        h2.post-title Lorem ipsum
        div.post-meta
          time 2 napja
      img.post-image
      div.post-content
        p Lorem ipsum, dolor sit amet consectetur..
  aside.sidebar
    h3 Keresés
    form
      input
      input
    h3 Kategóriák
    ul
      li
        a Autók 
          span 3
  footer.footer
    a Vissza az oldal tetejére
```

A HTML tag-ek viszonyát behúzásokkal jelöltük. Tehát az alábbi kód 

```jade
header.header
  div.container
    h1.logo Your logo
```

az alábbi HTML kódot reprezentálja:

```
<header class="header">
  <div class="container">
    <h1 class="logo">Your Logo</h1>
  </div>
</header>
```

Ez alapján elkészíhető a feladatban kért oldal.

