# Forms

## Get All forms

This endpoint retrieves an array of all forms.

### HTTP Request

`GET https://example.com/wp-json/frm/v2/forms`

```shell
curl -user 95SX-LM4Z-DDTC-HP8A:x https://example.com/wp-json/frm/v2/forms
```

```php
<?php
$headers = array (
	'Authorization' => 'Basic ' . base64_encode( '95SX-LM4Z-DDTC-HP8A:x' ),
);

$response = wp_remote_request( 'https://example.com/wp-json/frm/v2/forms', array(
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
		url: "https://example.com/jonathan/wp-json/frm/v2/forms",
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
  "3qshv": {
    "id": "40",
    "form_key": "3qshv",
    "name": "Example Form",
    "description": "",
    "parent_form_id": "0",
    "logged_in": "0",
    "is_template": "0",
    "created_at": "2017-05-15 05:28:46",
    "link": "https://example.com/wp-admin/admin-ajax.php?action=frm_forms_preview&#038;form=3qshv",
    "_links": {
      "self": [
        {
          "href": "https://example.com/wp-json/frm/v2/forms/40"
        }
      ],
      "collection": [
        {
          "href": "https://example.com/wp-json/frm/v2/forms"
        }
      ],
      "fields": [
        {
          "embeddable": true,
          "href": "https://example.com/wp-json/frm/v2/forms/40/fields"
        }
      ]
    }
  }
}
```

### Query Parameters

Parameter | Default | Description
--------- | ------- | -----------
limit | 20 | Limit the number of forms returned
order | ASC | Use ASC or DESC
order_by | created_at | Order the entries by id, created_at, updated_at, form_id
page | 1 | The page number to retrieve.
page_size | 10 | Change the number of forms returned per page
return | array | Use ?return=html to return HTML instead of JSON
search | '' | Search all fields in the entries for a value.

### Pagination

Requests that return multiple items will be paginated to 10 items by default. The items per page can be specified with the `?page_size` parameter:

`GET /forms?page_size=15`

You can specify further pages with the `?page` parameter:

`GET /forms?page=2`

## Get a Single Form

This endpoint gets a single form.

`GET https://example.com/wp-json/frm/v2/forms/{formID}`

```shell
curl -user 95SX-LM4Z-DDTC-HP8A:x https://example.com/wp-json/frm/v2/forms/40
```

```php
<?php
$headers = array (
	'Authorization' => 'Basic ' . base64_encode( '95SX-LM4Z-DDTC-HP8A:x' ),
);

$response = wp_remote_request( 'https://example.com/wp-json/frm/v2/forms/40', array(
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
		url: "https://example.com/jonathan/wp-json/frm/v2/forms/40",
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
  "id": "40",
  "form_key": "3qshv",
  "name": "Example Form",
  "description": "",
  "parent_form_id": "0",
  "logged_in": "0",
  "is_template": "0",
  "created_at": "2017-05-15 05:28:46",
  "link": "https://example.com/wp-admin/admin-ajax.php?action=frm_forms_preview&#038;form=3qshv",
  "_links": {
    "self": [
      {
        "href": "https://example.com/wp-json/frm/v2/forms/40"
      }
    ],
    "collection": [
      {
        "href": "https://example.com/wp-json/frm/v2/forms"
      }
    ],
    "fields": [
      {
        "embeddable": true,
        "href": "https://example.com/wp-json/frm/v2/forms/40/fields"
      }
    ]
  }
}
```

## Create a Form

This endpoint creates a single form.

`POST http://example.com/wp-json/frm/v2/forms/`

```shell
curl -user 95SX-LM4Z-DDTC-HP8A:x -X POST https://example.com/wp-json/frm/v2/forms
```

```php
<?php
$headers = array (
	'Authorization' => 'Basic ' . base64_encode( '95SX-LM4Z-DDTC-HP8A:x' ),
);

$response = wp_remote_request( 'https://example.com/wp-json/frm/v2/forms', array(
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
		url: "https://example.com/wp-json/frm/v2/forms",
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
    "id": "40",
    "form_key": "3qshv",
    "name": "",
    "description": "",
    "status": "draft",
    "parent_form_id": "0",
    "logged_in": "0",
    "is_template": "0",
    "options": {
        "submit_value": "Submit",
        "success_action": "message",
        "success_msg": "Your responses were successfully submitted. Thank you!",
        "show_form": 0,
        "akismet": "",
        "no_save": 0,
        "ajax_load": 0,
        "form_class": "",
        "custom_style": 1,
        "before_html": "<legend class=\"frm_hidden\">[form_name]</legend>\n[if form_name]<h3 class=\"frm_form_title\">[form_name]</h3>[/if form_name]\n[if form_description]<div class=\"frm_description\">[form_description]</div>[/if form_description]",
        "after_html": "",
        "submit_html": "<div class=\"frm_submit\">\n[if back_button]<button type=\"submit\" name=\"frm_prev_page\" formnovalidate=\"formnovalidate\" class=\"frm_prev_page\" [back_hook]>[back_label]</button>[/if back_button]\n<button class=\"frm_button_submit\" type=\"submit\"  [button_action]>[button_label]</button>\n[if save_draft]<a href=\"#\" class=\"frm_save_draft\" [draft_hook]>[draft_label]</a>[/if save_draft]\n</div>"
    },
    "editable": "0",
    "created_at": "2017-05-20 04:47:56",
    "link": "https://example.com/wp-admin/admin-ajax.php?action=frm_forms_preview&#038;form=3qshv",
    "_links": {
        "self": [
            {
                "href": "https://example.com/wp-json/frm/v2/forms/40"
            }
        ],
        "collection": [
            {
                "href": "https://example.com/wp-json/frm/v2/forms"
            }
        ],
        "fields": [
            {
                "embeddable": true,
                "href": "https://example.com/wp-json/frm/v2/forms/40/fields"
            }
        ]
    }
}
```

## Delete a Form

This endpoint deletes a single form.

`DELETE http://example.com/wp-json/frm/v2/forms/{formID}`

<aside class="warning">
Deleting a form with the endpoint will permanently and immediately delete the form and all of it's fields.
</aside>

```shell
curl -user 95SX-LM4Z-DDTC-HP8A:x -X DELETE https://example.com/wp-json/frm/v2/forms/40
```

```php
<?php
$headers = array (
	'Authorization' => 'Basic ' . base64_encode( '95SX-LM4Z-DDTC-HP8A:x' ),
);

$response = wp_remote_request( 'https://example.com/wp-json/frm/v2/forms/40', array(
	'method' => 'DELETE',
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
		method: "DELETE",
		url: "https://example.com/wp-json/frm/v2/forms/40",
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
    "id": "40",
    "form_key": "3qshv",
    "name": "Example Form",
    "description": "",
    "status": "draft",
    "parent_form_id": "0",
    "logged_in": "0",
    "is_template": "0",
    "options": {
        "submit_value": "Submit",
        "success_action": "message",
        "success_msg": "Your responses were successfully submitted. Thank you!",
        "show_form": 0,
        "akismet": "",
        "no_save": 0,
        "ajax_load": 0,
        "form_class": "",
        "custom_style": 1,
        "before_html": "<legend class=\"frm_hidden\">[form_name]</legend>\n[if form_name]<h3 class=\"frm_form_title\">[form_name]</h3>[/if form_name]\n[if form_description]<div class=\"frm_description\">[form_description]</div>[/if form_description]",
        "after_html": "",
        "submit_html": "<div class=\"frm_submit\">\n[if back_button]<button type=\"submit\" name=\"frm_prev_page\" formnovalidate=\"formnovalidate\" class=\"frm_prev_page\" [back_hook]>[back_label]</button>[/if back_button]\n<button class=\"frm_button_submit\" type=\"submit\"  [button_action]>[button_label]</button>\n[if save_draft]<a href=\"#\" class=\"frm_save_draft\" [draft_hook]>[draft_label]</a>[/if save_draft]\n</div>"
    },
    "editable": "0",
    "created_at": "2017-05-20 04:47:56",
    "link": "https://example.com/wp-admin/admin-ajax.php?action=frm_forms_preview&#038;form=3qshv",
    "_links": {
        "self": [
            {
                "href": "https://example.com/wp-json/frm/v2/forms/568"
            }
        ],
        "collection": [
            {
                "href": "https://example.com/wp-json/frm/v2/forms"
            }
        ],
        "fields": [
            {
                "embeddable": true,
                "href": "https://example.com/wp-json/frm/v2/forms/568/fields"
            }
        ]
    }
}
```
