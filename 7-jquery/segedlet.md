# JQuery
- Libary DOM manipulációhoz és eseménykezeléshez (és még sok máshoz)
- `$()` függvény a belépési pont
- `$(document)` jquery objektummá alakítás (minden dom elementre megy)
  - függvények paraméter nélkül általában lekérdezést jelentenek 

## DOM bejárás
- CSS selectorokat használhatunk
  - `$('li')`
  - `$('.post')`
  - `$('#container')`
  - `$('.post.active')`
  - `$('ul #menu li a ')`
- innerText, innerHTML helyett `text(), html()`

## DOM manipuláció
- `$('.post').show()`  `$('.post').hide()`
- `$('.post').css('background-color', 'red')`
- `$('.post').text('Hello world');`
- `$('.post').append('Hello world');`


## Események
- `on('event', handler)`

  ```javascript
  $('.button').on('click', function(){
  	...
  });
  ```

- Létezik rövidebb forma is: `click(handler)`, `mouseenter(handler)`, stb

  ```javascript
  $('.button').click(function(){
  	...
  });
  ```

- `$(this)` mindig a fogadó elemre mutat

  ```javascript
  $('.button').click(function(){
      $(this).css('background-color', 'red');
  });
  ```


## AJAX
- Asynchronous JavaScript and XML
- Régen használták az XML-t, ma már inkább csak JSON
- Háttérben, az oldal teljes újratöltése nélkül lehet a serverrel adatot cserélni

## JSON
- Egyszerű szöveges formátum
- JavaScript-ből remekül használható

```json
{
  "nev": "Kovács János",
  "kor": 25,
  "cim":
 {
    "utcaHazszam": "2. utca 21.",
    "varos": "New York",
    "allam": "NY",
    "iranyitoSzam": "10021"
   },
  "telefonSzam":
  [
    {
      "tipus": "otthoni",
      "szam": "212 555-1234"
    },
    {
     "tipus": "fax",
      "szam": "646 555-4567"
    }
  ]
}
```

## JQuery AJAX

Példa GET kérésre

```javascript
$.ajax({
    url: '/users',
    method: 'GET',
    success: function (data) {
        console.log(data);
    }
});
```

Példa POST kérésre

```
var nameInput = $('input[name="name"]).val();
$.ajax({
    url: '/users',
    method: 'POST',
    data: {
        name: nameInput
    }
    success: function (data) {
        console.log(data);
    }
});
```

