# Entries

## Get All Entries

This endpoint retrieves all entries.

### HTTP Request

`GET http://example.com/wp-json/frm/v2/entries`

```shell
curl -user 95SX-LM4Z-DDTC-HP8A:x https://example.com/wp-json/frm/v2/entries
```

```php
<?php
$headers = array (
	'Authorization' => 'Basic ' . base64_encode( '95SX-LM4Z-DDTC-HP8A:x' ),
);

$response = wp_remote_request( 'https://example.com/wp-json/frm/v2/entries', array(
	'method' => 'GET',
	'headers' => $headers
));
?>
```

```javascript
jQuery(document).ready(function($) {
	$.ajax({
		beforeSend: function(xhr){
			xhr.setRequestHeader ("Authorization", "Basic " + btoa("95SX-LM4Z-DDTC-HP8A:x"));
		},
		dataType: "json",
		url: "https://example.com/jonathan/wp-json/frm/v2/entries",
		success: function(json){
			//do something with the json
			console.log(json);
		}
	});
});
```

> JSON response example:

```json
{
    "sxmwc": {
        "id": "4119",
        "item_key": "sxmwc",
        "name": "test",
        "ip": "70.250.112.193",
        "meta": {
            "enfr": "test"
        },
        "form_id": "53",
        "post_id": "0",
        "user_id": "6",
        "parent_item_id": "0",
        "is_draft": "0",
        "updated_by": "6",
        "created_at": "2017-06-05 06:05:34",
        "updated_at": "2017-06-10 23:14:20"
    }
}
```

### Query Parameters

Parameter | Default | Description
--------- | ------- | -----------
form_id | 0 | Get all entries from a specific form
page | 1 | The page number to retrieve.
page_size | 25 | Change the number of entries returned
order | ASC | Use ASC or DESC
order_by | id | Order the entries by id, created_at, updated_at, form_id
search | | Search all fields in the entries for a value.

<aside class="notice">
Instead of using GET http://example.com/wp-json/frm/v2/entries?form_id=1 to get all entries from a specific form, you could also use the following HTTP Request.
</aside>

`GET http://example.com/wp-json/frm/v2/forms/1/entries`

### Pagination

Requests that return multiple items will be paginated to 25 items by default. The items per page can be specified with the `?page_size` parameter:

`GET /entries?page_size=15`

You can specify further pages with the `?page` parameter:

`GET /entries?page=2`

## Get a single entry by Entry ID ##

This endpoint retrieves a single entry using the Entry ID.

### HTTP Request ###

`GET http://example.com/wp-json/frm/v2/entries/{entryID}`

```shell
curl -user 95SX-LM4Z-DDTC-HP8A:x https://example.com/wp-json/frm/v2/entries/4119
```

```php
<?php
$headers = array (
	'Authorization' => 'Basic ' . base64_encode( '95SX-LM4Z-DDTC-HP8A:x' ),
);

$response = wp_remote_request( 'https://example.com/wp-json/frm/v2/entries/4119', array(
	'method' => 'GET',
	'headers' => $headers
));
?>
```

```javascript
jQuery(document).ready(function($) {
	$.ajax({
		beforeSend: function(xhr){
			xhr.setRequestHeader ("Authorization", "Basic " + btoa("95SX-LM4Z-DDTC-HP8A:x"));
		},
		dataType: "json",
		url: "https://example.com/jonathan/wp-json/frm/v2/entries/4119",
		success: function(json){
			//do something with the json
			console.log(json);
		}
	});
});
```

> JSON response example:

```json
{
    "id": "4119",
    "item_key": "sxmwc",
    "name": "test",
    "ip": "70.250.112.193",
    "meta": {
        "enfr": "test"
    },
    "form_id": "53",
    "post_id": "0",
    "user_id": "6",
    "parent_item_id": "0",
    "is_draft": "0",
    "updated_by": "6",
    "created_at": "2017-06-05 06:05:34",
    "updated_at": "2017-06-10 23:14:20"
}
```

## Create a single entry ##

This endpoint creates a single entry.

### HTTP Request ###

`POST http://example.com/wp-json/frm/v2/entries/`

```shell
curl -user 95SX-LM4Z-DDTC-HP8A:x -X POST https://example.com/wp-json/frm/v2/entries
```

```php
<?php
$headers = array (
	'Authorization' => 'Basic ' . base64_encode( '95SX-LM4Z-DDTC-HP8A:x' ),
);

$response = wp_remote_request( 'https://example.com/wp-json/frm/v2/entries', array(
	'method' => 'POST',
	'headers' => $headers
));
?>
```

```javascript
jQuery(document).ready(function($) {
	$.ajax({
		beforeSend: function(xhr){
			xhr.setRequestHeader ("Authorization", "Basic " + btoa("95SX-LM4Z-DDTC-HP8A:x"));
		},
		dataType: "json",
    method: "POST",
		url: "https://example.com/jonathan/wp-json/frm/v2/entries",
		success: function(json){
			//do something with the json
			console.log(json);
		}
	});
});
```

> JSON response example:

```json
// create example
```

## Update a single entry by Entry ID ##

These endpoints update a single entry.

### HTTP Request ###

`PUT http://example.com/wp-json/frm/v2/entries/{entryID}`

```shell
curl -user 95SX-LM4Z-DDTC-HP8A:x -X PUT https://example.com/wp-json/frm/v2/entries/4119
```

```php
<?php
$headers = array (
	'Authorization' => 'Basic ' . base64_encode( '95SX-LM4Z-DDTC-HP8A:x' ),
);

$response = wp_remote_request( 'https://example.com/wp-json/frm/v2/entries/4119', array(
	'method' => 'PUT',
	'headers' => $headers
));
?>
```

```javascript
jQuery(document).ready(function($) {
	$.ajax({
		beforeSend: function(xhr){
			xhr.setRequestHeader ("Authorization", "Basic " + btoa("95SX-LM4Z-DDTC-HP8A:x"));
		},
		dataType: "json",
    method: "PUT",
		url: "https://example.com/jonathan/wp-json/frm/v2/entries/4119",
		success: function(json){
			//do something with the json
			console.log(json);
		}
	});
});
```

> JSON response example:

```json
// add an example
```
