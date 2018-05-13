# Custom Perk Redemptions By User

## [GET] Get All Custom Perk Redemptions for a User

```shell
curl "http://portify-api.herokuapp.com/companies/:company_id/admins/:admin_id/users/:user_id/custom_perk_redemptions"
  -H "Authorization": "Token token=yourtoken"
```

> The above command returns JSON structured like this:

```json
{
  "custom_perk_redemptions": [
    {
      "user_id": "951e28bf-a506-4668-928c-814764c903c7",
      "custom_perk_id": "02628317-abbd-4b4a-a38d-adb20f374e57",
      "created_at": "2018-03-21 14:57:50.000"
    },
    {
      "user_id": "951e28bf-a506-4668-928c-814764c903c7",
      "custom_perk_id": "02628317-abbd-4b4a-a38d-adb20f374e57",
      "created_at": "2018-03-28 15:13:12.010"
    },
  ]
}
```

This endpoint retrieves all custom perk redemptions for a specific user.

### URL Parameters

Parameter | Description
--------- | -----------
company_id | The ID of your company
admin_id | The ID of your admin account
user_id | The ID of the user