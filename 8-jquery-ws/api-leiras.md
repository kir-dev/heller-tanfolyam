# API leírás

## Bejegyzések listázása
`GET /articles`

```json
[
    {
        "id": 1,
        "title": "Lorem ipsum",
        "intro": "Lorem ipsum dolor set amet",
        "created_at": "2018-11-19T11:57:35.202Z",
        "updated_at": "2018-11-19T11:57:35.202Z"
    },
    {
        "id": 2,
        "title": "Lorem ipsum 2",
        "intro": "Lorem ipsum dolor set amet",
        "created_at": "2018-11-18T11:57:35.202Z",
        "updated_at": "2018-11-18T11:57:35.202Z"
    }
]
```

## Bejegyzések megtekintése
`GET /articles/{id}`

```json

{
    "id": 1,
    "title": "Lorem ipsum",
    "intro": "Lorem ipsum dolor set amet",
    "content": "Lorem ipsum dooooooooooooo",
    "created_at": "2018-11-19T11:57:35.202Z",
    "updated_at": "2018-11-19T11:57:35.202Z"
}
```

## Új bejegyzés

`POST /articles`

Kérés
```json
{
	"title": "Lorem ipsum",
	"intro": "Lorem ipsum dolor set amet",
	"content": "Lorem ipsum dooooooooooooo"
}
```

Válasz
```json
{
    "id": 1,
    "title": "Lorem ipsum",
    "intro": "Lorem ipsum dolor set amet",
    "content": "Lorem ipsum dooooooooooooo",
    "created_at": "2018-11-19T11:57:35.202Z",
    "updated_at": "2018-11-19T11:57:35.202Z"
}
```


## Bejegyzés szerkesztése

`POST /articles/{id}`

Kérés
```json
{
	"title": "Lorem ipsum edited",
	"intro": "Lorem ipsum dolor set amet edited",
	"content": "Lorem ipsum dooooooooooooo edited"
}
```

Válasz
```json
{
    "id": 1,
    "title": "Lorem ipsum edited",
    "intro": "Lorem ipsum dolor set amet edited",
    "content": "Lorem ipsum dooooooooooooo edited",
    "created_at": "2018-11-19T11:57:35.202Z",
    "updated_at": "2018-11-19T12:01:18.503Z"
}
```



---

## Kommentek listázása

`GET /articles/{article_id}/comments`

Válasz

```json
[
    {
        "id": 1,
        "name": "Példa János",
        "article_id": 1,
        "content": "Ez érdekes cikk volt",
        "created_at": "2018-11-19T11:57:35.202Z",
        "updated_at": "2018-11-19T11:57:35.202Z"
    },
    {
        "id": 2,
        "name": "Teszt Elek",
        "article_id": 1,
        "content": "Hello",
        "created_at": "2018-11-18T11:57:35.202Z",
        "updated_at": "2018-11-18T11:57:35.202Z"
    }
]
```

## Komment létrehozása

`POST /articles/{article_id}/comments`

Kérés

```json
{
    "name": "Példa János",
    "content": "Ez érdekes cikk volt",
}
```

Válasz

```json
{
    "id": 1,
    "name": "Példa János",
    "article_id": 1,
    "content": "Ez érdekes cikk volt",
    "created_at": "2018-11-19T11:57:35.202Z",
    "updated_at": "2018-11-19T11:57:35.202Z"
}
```

