# Freebies

## [GET] Get All Freebies

```shell
curl "http://portify-api.herokuapp.com/companies/:company_id/admins/:admin_id/freebies?enrolment_id=..."
  -H "Authorization": "Token token=yourtoken"
```

> The above command returns JSON structured like this:

```json
{
  "freebies": [
    {
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
    }
  ]
}
```

This endpoint retrieves all freebies, optionally filtered by an enrolment_id.

### URL Parameters

Parameter | Description
--------- | -----------
company_id | The ID of your company
admin_id | The ID of your admin account
enrolment_id | The ID of an enrolment to filter by (optional)