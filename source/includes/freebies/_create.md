## [POST] Create a Freebie

```shell
curl "http://portify-api.herokuapp.com/companies/:company_id/admins/:admin_id/freebies"
  -X POST
  -H "Authorization": "Token token=yourtoken"
  -H "Accept": "application/json"
  -H "Content-Type": "application/json"
  -d '{
    "freebie": {
		  "enrolment_id": "76050eab-1c74-47db-a602-652c649a9110",
		  "perk_id": "906188c9-7bb1-4502-b882-fa207aafb1c6",
		  "value": "5",
		  "message": "Congratulations of being one of the top performing riders!"
		}
	}'
```
> The above command returns JSON structured like this:

```json
{
	"freebie": {
    "id": "d4049a3e-ce5e-4d16-92ba-22e133a4fb48",
    "enrolment_id": "76050eab-1c74-47db-a602-652c649a9110",
    "perk_id": "906188c9-7bb1-4502-b882-fa207aafb1c6",
    "value": "5",
    "redeemed": false,
    "expires_on": null,
    "message": "Congratulations of being one of the top performing riders!",
    "perk": {
      "id": "906188c9-7bb1-4502-b882-fa207aafb1c6",
      "title": "5% off at Amazon"
    },
    "created_at": "2018-05-03 15:22:50.000"
  },
  "message": { 
		"type": "success", 
		"text": "Freebie Created Successfully!", 
		"code": "freebie_create_success" 
	}
}
```

This endpoint creates a new freebie.

### URL Parameters

Parameter | Description
--------- | -----------
company_id | The ID of your company
admin_id | The ID of your admin account
