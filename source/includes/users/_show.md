## [GET] Get a Specific USer

```shell
curl "http://portify-api.herokuapp.com/companies/:company_id/admins/:admin_id/users/:id"
  -H "Authorization": "Token token=yourtoken"
```

> The above command returns JSON structured like this:

```json
{
	"user": {
    "id": "02628317-abbd-4b4a-a38d-adb20f374e57",
    "name": "Chris Butcher",
    "email": "chris@portify.co",
    "phone": "07500802406",
    "created_at": "2018-03-21 14:57:50.000"
  }
}
```

This endpoint retrieves a specific enrolment.

### URL Parameters

Parameter | Description
--------- | -----------
company_id | The ID of your company
admin_id | The ID of your admin account
id | The ID of the user to show
