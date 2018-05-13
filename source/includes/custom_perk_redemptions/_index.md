# Custom Perk Redemptions

## [GET] Get All Redemptions for a Custom Perk

```shell
curl "http://portify-api.herokuapp.com/companies/:company_id/admins/:admin_id/custom_perks/:custom_perk_id/custom_perk_redemptions"
  -H "Authorization": "Token token=yourtoken"
```

> The above command returns JSON structured like this:

```json
{
  "custom_perk_redemptions": [
    {
      "custom_perk_id": "906188c9-7bb1-4502-b882-fa207aafb1c6",
      "user_id": "02628317-abbd-4b4a-a38d-adb20f374e57",
      "created_at": "2018-03-21 14:57:50.000"
    },
    {
      "custom_perk_id": "ba445cb5-6887-40c9-8eb2-6f6344558391",
      "user_id": "951e28bf-a506-4668-928c-814764c903c7",
      "created_at": "2018-01-04 15:57:22.000"
    },
  ]
}
```

This endpoint retrieves all redemptions for a specific custom perk.

### URL Parameters

Parameter | Description
--------- | -----------
company_id | The ID of your company
admin_id | The ID of your admin account
custom_perk_id | The ID of the custom perk