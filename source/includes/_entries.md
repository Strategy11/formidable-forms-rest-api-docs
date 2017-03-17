# Entries

## Get All Entries

This endpoint retrieves all entries.

```python
import kittn

api = kittn.authorize('meowmeowmeow')
api.kittens.get()
```

```javascript
const kittn = require('kittn');

let api = kittn.authorize('meowmeowmeow');
let kittens = api.kittens.get();
```

> The above command returns JSON structured like this:

```json
[
  {
    "id": 1,
    "name": "Fluffums",
    "breed": "calico",
    "fluffiness": 6,
    "cuteness": 7
  },
  {
    "id": 2,
    "name": "Max",
    "breed": "unknown",
    "fluffiness": 5,
    "cuteness": 10
  }
]
```

### HTTP Request

`GET http://example.com/wp-json/frm/v2/entries`

### Query Parameters

Parameter | Default | Description
--------- | ------- | -----------
order_by | id | Order the entries by id, created_at, updated_at, form_id
order | ASC | Use ASC or DESC
page | 1 | The page number to retrieve.
page_size | 25 | Change the number of entries returned
search | | Search all fields in the entries for a value.

### Pagination

Requests that return multiple items will be paginated to 25 items by default. The items per page can be specified with the `?page_size` parameter:

`GET /entries?page_size=15`

You can specify further pages with the `?page` parameter:

`GET /entries?page=2`
