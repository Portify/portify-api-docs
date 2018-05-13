## [DELETE] Delete a Specific Custom Perk

```shell
curl "http://portify-api.herokuapp.com/companies/:company_id/admins/:admin_id/custom_perks/:id"
  -X DELETE
  -H "Authorization": "Token token=yourtoken"
```

> The above command returns JSON structured like this:

```json
{
  "id": "906188c9-7bb1-4502-b882-fa207aafb1c6",
	"message": { 
		"type": "success", 
		"text": "Perk Deleted Successfully!", 
		"code": "perk_delete_success" 
	}
}
```

This endpoint retrieves a deletes a custom perk.

### URL Parameters

Parameter | Description
--------- | -----------
company_id | The ID of your company
admin_id | The ID of your admin account
id | The ID of the perk to delete


