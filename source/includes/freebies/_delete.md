## [DELETE] Delete a Specific Freebie

```shell
curl "http://portify-api.herokuapp.com/companies/:company_id/admins/:admin_id/freebies/:id"
  -X DELETE
  -H "Authorization": "Token token=yourtoken"
```

> The above command returns JSON structured like this:

```json
{
  "id": "d4049a3e-ce5e-4d16-92ba-22e133a4fb48",
	"message": { 
		"type": "success", 
		"text": "Freebie Deleted Successfully!", 
		"code": "freebie_delete_success" 
	}
}
```

This endpoint a deletes a freebie.

### URL Parameters

Parameter | Description
--------- | -----------
company_id | The ID of your company
admin_id | The ID of your admin account
id | The ID of the freebie to delete


