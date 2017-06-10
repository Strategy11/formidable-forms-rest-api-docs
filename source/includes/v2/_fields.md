# Fields #

## Get All Fields from a Form ##

This endpoint will get an array of all fields from a single form.

### HTTP Request ###

`GET http://example.com/wp-json/frm/v2/forms/{formID}/fields`

### Query Parameters ###

There are no query parameters at this time.

```shell
curl -user 95SX-LM4Z-DDTC-HP8A:x https://example.com/wp-json/frm/v2/forms/40/fields
```

```php
<?php
$headers = array (
	'Authorization' => 'Basic ' . base64_encode( '95SX-LM4Z-DDTC-HP8A:x' ),
);

$response = wp_remote_request( 'https://example.com/wp-json/frm/v2/forms/40/fields', array(
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
		url: "https://example.com/jonathan/wp-json/frm/v2/forms/40/fields",
		success: function(json){
			//do something with the json
			console.log(json);
		}
	});
});
```

```json
{
    "atkg5": {
        "id": "686",
        "field_key": "atkg5",
        "name": "Dropdown",
        "description": "",
        "type": "select",
        "default_value": "",
        "options": [
            {
                "label": "",
                "value": ""
            },
            {
                "label": "Option 1",
                "value": "Option 1"
            }
        ],
        "field_order": "0",
        "required": "0",
        "field_options": {
            "size": "",
            "max": "",
            "label": "",
            "blank": "This field cannot be blank.",
            "required_indicator": "*",
            "invalid": "",
            "separate_value": 0,
            "clear_on_focus": 0,
            "default_blank": "0",
            "classes": "",
            "custom_html": "<div id=\"frm_field_[id]_container\" class=\"frm_form_field form-field [required_class][error_class]\">\r\n    <label for=\"field_[key]\" class=\"frm_primary_label\">[field_name]\r\n        <span class=\"frm_required\">[required_label]</span>\r\n    </label>\r\n    [input]\r\n    [if description]<div class=\"frm_description\">[description]</div>[/if description]\r\n    [if error]<div class=\"frm_error\">[error]</div>[/if error]\r\n</div>",
            "captcha_size": "normal",
            "captcha_theme": "light",
            "in_section": "0",
            "slide": 0,
            "form_select": "",
            "show_hide": "show",
            "any_all": "any",
            "align": "block",
            "hide_field": [],
            "hide_field_cond": [
                "=="
            ],
            "hide_opt": [],
            "star": 0,
            "ftypes": [],
            "data_type": "select",
            "restrict": 0,
            "start_year": 2000,
            "end_year": 2020,
            "read_only": 0,
            "admin_only": "",
            "locale": "",
            "attach": false,
            "minnum": 0,
            "maxnum": 9999,
            "delete": false,
            "step": 1,
            "clock": 12,
            "single_time": 0,
            "start_time": "00:00",
            "end_time": "23:59",
            "unique": 0,
            "use_calc": 0,
            "calc": "",
            "calc_dec": "",
            "calc_type": "",
            "dyn_default_value": "",
            "multiple": 0,
            "unique_msg": "",
            "autocom": 0,
            "format": "",
            "repeat": 0,
            "add_label": "Add",
            "remove_label": "Remove",
            "conf_field": "",
            "conf_input": "",
            "conf_desc": "",
            "conf_msg": "The entered values do not match",
            "other": "0",
            "autopopulate_value": false,
            "get_values_form": "",
            "get_values_field": "",
            "watch_lookup": [
                ""
            ],
            "get_most_recent_value": "",
            "lookup_filter_current_user": false,
            "custom_field": "",
            "post_field": "",
            "taxonomy": "category",
            "exclude_cat": 0
        },
        "created_at": "2017-06-05 06:04:54"
    },
    "enfr": {
        "id": "685",
        "field_key": "enfr",
        "name": "Single Line Text",
        "description": "",
        "type": "text",
        "default_value": "",
        "options": "",
        "field_order": "1",
        "required": "0",
        "field_options": {
            "size": "",
            "max": "",
            "label": "",
            "blank": "This field cannot be blank.",
            "required_indicator": "*",
            "invalid": "",
            "separate_value": 0,
            "clear_on_focus": "0",
            "default_blank": "0",
            "classes": "",
            "custom_html": "<div id=\"frm_field_[id]_container\" class=\"frm_form_field form-field [required_class][error_class]\">\r\n    <label for=\"field_[key]\" class=\"frm_primary_label\">[field_name]\r\n        <span class=\"frm_required\">[required_label]</span>\r\n    </label>\r\n    [input]\r\n    [if description]<div class=\"frm_description\">[description]</div>[/if description]\r\n    [if error]<div class=\"frm_error\">[error]</div>[/if error]\r\n</div>",
            "captcha_size": "normal",
            "captcha_theme": "light",
            "in_section": "0",
            "slide": 0,
            "form_select": "",
            "show_hide": "show",
            "any_all": "any",
            "align": "block",
            "hide_field": [],
            "hide_field_cond": [
                "=="
            ],
            "hide_opt": [],
            "star": 0,
            "ftypes": [],
            "data_type": "select",
            "restrict": 0,
            "start_year": 2000,
            "end_year": 2020,
            "read_only": 0,
            "admin_only": "",
            "locale": "",
            "attach": false,
            "minnum": 0,
            "maxnum": 9999,
            "delete": false,
            "step": 1,
            "clock": 12,
            "single_time": 0,
            "start_time": "00:00",
            "end_time": "23:59",
            "unique": 0,
            "use_calc": 0,
            "calc": "",
            "calc_dec": "",
            "calc_type": "",
            "dyn_default_value": "",
            "multiple": 0,
            "unique_msg": "",
            "autocom": 0,
            "format": "",
            "repeat": 0,
            "add_label": "Add",
            "remove_label": "Remove",
            "conf_field": "",
            "conf_input": "",
            "conf_desc": "",
            "conf_msg": "The entered values do not match",
            "other": 0,
            "autopopulate_value": false,
            "get_values_form": "",
            "get_values_field": "",
            "watch_lookup": [
                ""
            ],
            "get_most_recent_value": "",
            "lookup_filter_current_user": false,
            "custom_field": "",
            "post_field": "",
            "taxonomy": "category",
            "exclude_cat": 0
        },
        "created_at": "2017-06-05 06:04:51"
    }
}
```

## Create a Field in a Form ##

This endpoint will allow you to create a field in a form.

### HTTP Request ###

`POST http://example.com/wp-json/frm/v2/forms/{formID}/fields`

```shell
curl -user 95SX-LM4Z-DDTC-HP8A:x https://example.com/wp-json/frm/v2/forms/40/fields
```

```php
<?php
$headers = array (
	'Authorization' => 'Basic ' . base64_encode( '95SX-LM4Z-DDTC-HP8A:x' ),
);

$response = wp_remote_request( 'https://example.com/wp-json/frm/v2/forms/40/fields', array(
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
		url: "https://example.com/jonathan/wp-json/frm/v2/forms/40/fields",
		success: function(json){
			//do something with the json
			console.log(json);
		}
	});
});
```

```json
{
    "atkg5": {
        "id": "686",
        "field_key": "atkg5",
        "name": "Dropdown",
        "description": "",
        "type": "select",
        "default_value": "",
        "options": [
            {
                "label": "",
                "value": ""
            },
            {
                "label": "Option 1",
                "value": "Option 1"
            }
        ],
        "field_order": "0",
        "required": "0",
        "field_options": {
            "size": "",
            "max": "",
            "label": "",
            "blank": "This field cannot be blank.",
            "required_indicator": "*",
            "invalid": "",
            "separate_value": 0,
            "clear_on_focus": 0,
            "default_blank": "0",
            "classes": "",
            "custom_html": "<div id=\"frm_field_[id]_container\" class=\"frm_form_field form-field [required_class][error_class]\">\r\n    <label for=\"field_[key]\" class=\"frm_primary_label\">[field_name]\r\n        <span class=\"frm_required\">[required_label]</span>\r\n    </label>\r\n    [input]\r\n    [if description]<div class=\"frm_description\">[description]</div>[/if description]\r\n    [if error]<div class=\"frm_error\">[error]</div>[/if error]\r\n</div>",
            "captcha_size": "normal",
            "captcha_theme": "light",
            "in_section": "0",
            "slide": 0,
            "form_select": "",
            "show_hide": "show",
            "any_all": "any",
            "align": "block",
            "hide_field": [],
            "hide_field_cond": [
                "=="
            ],
            "hide_opt": [],
            "star": 0,
            "ftypes": [],
            "data_type": "select",
            "restrict": 0,
            "start_year": 2000,
            "end_year": 2020,
            "read_only": 0,
            "admin_only": "",
            "locale": "",
            "attach": false,
            "minnum": 0,
            "maxnum": 9999,
            "delete": false,
            "step": 1,
            "clock": 12,
            "single_time": 0,
            "start_time": "00:00",
            "end_time": "23:59",
            "unique": 0,
            "use_calc": 0,
            "calc": "",
            "calc_dec": "",
            "calc_type": "",
            "dyn_default_value": "",
            "multiple": 0,
            "unique_msg": "",
            "autocom": 0,
            "format": "",
            "repeat": 0,
            "add_label": "Add",
            "remove_label": "Remove",
            "conf_field": "",
            "conf_input": "",
            "conf_desc": "",
            "conf_msg": "The entered values do not match",
            "other": "0",
            "autopopulate_value": false,
            "get_values_form": "",
            "get_values_field": "",
            "watch_lookup": [
                ""
            ],
            "get_most_recent_value": "",
            "lookup_filter_current_user": false,
            "custom_field": "",
            "post_field": "",
            "taxonomy": "category",
            "exclude_cat": 0
        },
        "created_at": "2017-06-05 06:04:54"
    },
    "enfr": {
        "id": "685",
        "field_key": "enfr",
        "name": "Single Line Text",
        "description": "",
        "type": "text",
        "default_value": "",
        "options": "",
        "field_order": "1",
        "required": "0",
        "field_options": {
            "size": "",
            "max": "",
            "label": "",
            "blank": "This field cannot be blank.",
            "required_indicator": "*",
            "invalid": "",
            "separate_value": 0,
            "clear_on_focus": "0",
            "default_blank": "0",
            "classes": "",
            "custom_html": "<div id=\"frm_field_[id]_container\" class=\"frm_form_field form-field [required_class][error_class]\">\r\n    <label for=\"field_[key]\" class=\"frm_primary_label\">[field_name]\r\n        <span class=\"frm_required\">[required_label]</span>\r\n    </label>\r\n    [input]\r\n    [if description]<div class=\"frm_description\">[description]</div>[/if description]\r\n    [if error]<div class=\"frm_error\">[error]</div>[/if error]\r\n</div>",
            "captcha_size": "normal",
            "captcha_theme": "light",
            "in_section": "0",
            "slide": 0,
            "form_select": "",
            "show_hide": "show",
            "any_all": "any",
            "align": "block",
            "hide_field": [],
            "hide_field_cond": [
                "=="
            ],
            "hide_opt": [],
            "star": 0,
            "ftypes": [],
            "data_type": "select",
            "restrict": 0,
            "start_year": 2000,
            "end_year": 2020,
            "read_only": 0,
            "admin_only": "",
            "locale": "",
            "attach": false,
            "minnum": 0,
            "maxnum": 9999,
            "delete": false,
            "step": 1,
            "clock": 12,
            "single_time": 0,
            "start_time": "00:00",
            "end_time": "23:59",
            "unique": 0,
            "use_calc": 0,
            "calc": "",
            "calc_dec": "",
            "calc_type": "",
            "dyn_default_value": "",
            "multiple": 0,
            "unique_msg": "",
            "autocom": 0,
            "format": "",
            "repeat": 0,
            "add_label": "Add",
            "remove_label": "Remove",
            "conf_field": "",
            "conf_input": "",
            "conf_desc": "",
            "conf_msg": "The entered values do not match",
            "other": 0,
            "autopopulate_value": false,
            "get_values_form": "",
            "get_values_field": "",
            "watch_lookup": [
                ""
            ],
            "get_most_recent_value": "",
            "lookup_filter_current_user": false,
            "custom_field": "",
            "post_field": "",
            "taxonomy": "category",
            "exclude_cat": 0
        },
        "created_at": "2017-06-05 06:04:51"
    }
}
```

## Get a Field from a Form ##

This endpoint will allow you to get a single field from a form.

### HTTP Request ###

`GET http://example.com/wp-json/frm/v2/forms/{formID}/fields/{fieldID}`

```shell
curl -user 95SX-LM4Z-DDTC-HP8A:x https://example.com/wp-json/frm/v2/forms/40/fields/686
```

```php
<?php
$headers = array (
	'Authorization' => 'Basic ' . base64_encode( '95SX-LM4Z-DDTC-HP8A:x' ),
);

$response = wp_remote_request( 'https://example.com/wp-json/frm/v2/forms/40/fields/686', array(
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
		url: "https://example.com/jonathan/wp-json/frm/v2/forms/40/fields/686",
		success: function(json){
			//do something with the json
			console.log(json);
		}
	});
});
```

```json
{
    "id": "686",
    "field_key": "atkg5",
    "name": "Dropdown",
    "description": "",
    "type": "select",
    "default_value": "",
    "options": [
        {
            "label": "",
            "value": ""
        },
        {
            "label": "Option 1",
            "value": "Option 1"
        }
    ],
    "field_order": "0",
    "required": "0",
    "field_options": {
        "size": "",
        "max": "",
        "label": "",
        "blank": "This field cannot be blank.",
        "required_indicator": "*",
        "invalid": "",
        "separate_value": 0,
        "clear_on_focus": 0,
        "default_blank": "0",
        "classes": "",
        "custom_html": "<div id=\"frm_field_[id]_container\" class=\"frm_form_field form-field [required_class][error_class]\">\r\n    <label for=\"field_[key]\" class=\"frm_primary_label\">[field_name]\r\n        <span class=\"frm_required\">[required_label]</span>\r\n    </label>\r\n    [input]\r\n    [if description]<div class=\"frm_description\">[description]</div>[/if description]\r\n    [if error]<div class=\"frm_error\">[error]</div>[/if error]\r\n</div>",
        "captcha_size": "normal",
        "captcha_theme": "light",
        "in_section": "0",
        "slide": 0,
        "form_select": "",
        "show_hide": "show",
        "any_all": "any",
        "align": "block",
        "hide_field": [],
        "hide_field_cond": [
            "=="
        ],
        "hide_opt": [],
        "star": 0,
        "ftypes": [],
        "data_type": "select",
        "restrict": 0,
        "start_year": 2000,
        "end_year": 2020,
        "read_only": 0,
        "admin_only": "",
        "locale": "",
        "attach": false,
        "minnum": 0,
        "maxnum": 9999,
        "delete": false,
        "step": 1,
        "clock": 12,
        "single_time": 0,
        "start_time": "00:00",
        "end_time": "23:59",
        "unique": 0,
        "use_calc": 0,
        "calc": "",
        "calc_dec": "",
        "calc_type": "",
        "dyn_default_value": "",
        "multiple": 0,
        "unique_msg": "",
        "autocom": 0,
        "format": "",
        "repeat": 0,
        "add_label": "Add",
        "remove_label": "Remove",
        "conf_field": "",
        "conf_input": "",
        "conf_desc": "",
        "conf_msg": "The entered values do not match",
        "other": "0",
        "autopopulate_value": false,
        "get_values_form": "",
        "get_values_field": "",
        "watch_lookup": [
            ""
        ],
        "get_most_recent_value": "",
        "lookup_filter_current_user": false,
        "custom_field": "",
        "post_field": "",
        "taxonomy": "category",
        "exclude_cat": 0
    },
    "created_at": "2017-06-05 06:04:54"
}
```

## Delete a Field from a Form ##

This endpoint will allow you to delete a single field from a form.

### HTTP Request ###

`DELETE http://example.com/wp-json/frm/v2/forms/{formID}/fields/{fieldID}`

```shell
curl -user 95SX-LM4Z-DDTC-HP8A:x https://example.com/wp-json/frm/v2/forms/40/fields/686
```

```php
<?php
$headers = array (
	'Authorization' => 'Basic ' . base64_encode( '95SX-LM4Z-DDTC-HP8A:x' ),
);

$response = wp_remote_request( 'https://example.com/wp-json/frm/v2/forms/40/fields/686', array(
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
    method: "DELETE",
		url: "https://example.com/jonathan/wp-json/frm/v2/forms/40/fields/686",
		success: function(json){
			//do something with the json
			console.log(json);
		}
	});
});
```

```json
{
    "id": "686",
    "field_key": "atkg5",
    "name": "Dropdown",
    "description": "",
    "type": "select",
    "default_value": "",
    "options": [
        {
            "label": "",
            "value": ""
        },
        {
            "label": "Option 1",
            "value": "Option 1"
        }
    ],
    "field_order": "0",
    "required": "0",
    "field_options": {
        "size": "",
        "max": "",
        "label": "",
        "blank": "This field cannot be blank.",
        "required_indicator": "*",
        "invalid": "",
        "separate_value": 0,
        "clear_on_focus": 0,
        "default_blank": "0",
        "classes": "",
        "custom_html": "<div id=\"frm_field_[id]_container\" class=\"frm_form_field form-field [required_class][error_class]\">\r\n    <label for=\"field_[key]\" class=\"frm_primary_label\">[field_name]\r\n        <span class=\"frm_required\">[required_label]</span>\r\n    </label>\r\n    [input]\r\n    [if description]<div class=\"frm_description\">[description]</div>[/if description]\r\n    [if error]<div class=\"frm_error\">[error]</div>[/if error]\r\n</div>",
        "captcha_size": "normal",
        "captcha_theme": "light",
        "in_section": "0",
        "slide": 0,
        "form_select": "",
        "show_hide": "show",
        "any_all": "any",
        "align": "block",
        "hide_field": [],
        "hide_field_cond": [
            "=="
        ],
        "hide_opt": [],
        "star": 0,
        "ftypes": [],
        "data_type": "select",
        "restrict": 0,
        "start_year": 2000,
        "end_year": 2020,
        "read_only": 0,
        "admin_only": "",
        "locale": "",
        "attach": false,
        "minnum": 0,
        "maxnum": 9999,
        "delete": false,
        "step": 1,
        "clock": 12,
        "single_time": 0,
        "start_time": "00:00",
        "end_time": "23:59",
        "unique": 0,
        "use_calc": 0,
        "calc": "",
        "calc_dec": "",
        "calc_type": "",
        "dyn_default_value": "",
        "multiple": 0,
        "unique_msg": "",
        "autocom": 0,
        "format": "",
        "repeat": 0,
        "add_label": "Add",
        "remove_label": "Remove",
        "conf_field": "",
        "conf_input": "",
        "conf_desc": "",
        "conf_msg": "The entered values do not match",
        "other": "0",
        "autopopulate_value": false,
        "get_values_form": "",
        "get_values_field": "",
        "watch_lookup": [
            ""
        ],
        "get_most_recent_value": "",
        "lookup_filter_current_user": false,
        "custom_field": "",
        "post_field": "",
        "taxonomy": "category",
        "exclude_cat": 0
    },
    "form_id": "53",
    "created_at": "2017-06-05 06:04:54"
}
```
