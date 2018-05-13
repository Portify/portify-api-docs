## [PATCH] Update a Specific Enrolment

```shell
curl "http://portify-api.herokuapp.com/companies/:company_id/admins/:admin_id/enrolments/:id"
  -X PATCH
  -H "Authorization": "Token token=yourtoken"
  -H "Accept": "application/json"
  -H "Content-Type": "application/json"
  -d '{
		"enrolment": {
		 	"active": false
		}
	}'
```

> The above command returns JSON structured like this:

```json
{
	"enrolment": {
		"id": "8190921a-d422-4d4d-ad95-84c5babfb40f",
		"user_id": null,
		"company_id": "39c01faf-94f9-44e5-98d9-d498b90b369a",
		"fixed_score": false,
		"score": null,
		"invited": true,
		"invite_email": "example@gmail.com",
		"invite_phone": "07500802406",
		"activation_code": "WH1X7",
		"active": false,
		"invite_email_last_sent": null,
		"created_at": "2018-02-02 13:23:18.000"
	},
	"message": { 
		"type": "success", 
		"text": "Enrolment Updated Successfully!", 
		"code": "enrolment_update_success" 
	}
}
```

This endpoint updates a specific enrolment, overwriting attributes specified in the body of the request.

### URL Parameters

Parameter | Description
--------- | -----------
company_id | The ID of your company
admin_id | The ID of your admin account
id | The ID of the enrolment