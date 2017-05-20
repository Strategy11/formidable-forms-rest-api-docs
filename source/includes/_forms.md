# Forms

## Get All forms

This endpoint retrieves an array of all forms.

### HTTP Request

`GET http://example.com/wp-json/frm/v2/forms`

### Query Parameters

Parameter | Default | Description
--------- | ------- | -----------
limit | 20 | Limit the number of forms returned
order | ASC | Use ASC or DESC
order_by | created_at | Order the entries by id, created_at, updated_at, form_id
page | 1 | The page number to retrieve.
page_size | 10 | Change the number of forms returned per page
return | array | Unknown
search | '' | Search all fields in the entries for a value.

### Pagination

Requests that return multiple items will be paginated to 10 items by default. The items per page can be specified with the `?page_size` parameter:

`GET /forms?page_size=15`

You can specify further pages with the `?page` parameter:

`GET /forms?page=2`

## Get a Single Form

This endpoint gets a single form.

`GET http://example.com/wp-json/frm/v2/forms/{formID}`

## Create a Form

This endpoint creates a single form.

`POST http://example.com/wp-json/frm/v2/forms/`

>The above command returns the following JSON.

```json
{
    "id": "568",
    "form_key": "65ukw",
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
    "link": "http://localhost:8888/wordpress/wp-admin/admin-ajax.php?action=frm_forms_preview&#038;form=65ukw",
    "_links": {
        "self": [
            {
                "href": "http://localhost:8888/wordpress/wp-json/frm/v2/forms/568"
            }
        ],
        "collection": [
            {
                "href": "http://localhost:8888/wordpress/wp-json/frm/v2/forms"
            }
        ],
        "fields": [
            {
                "embeddable": true,
                "href": "http://localhost:8888/wordpress/wp-json/frm/v2/forms/568/fields"
            }
        ]
    }
}
```

## Delete a Form

This endpoint deletes a single form.

`DELETE http://example.com/wp-json/frm/v2/forms/{formID}`
