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
      "created_at": "2018-03-21 14:57:50.000",
      "custom_perk": {
        "id": "02628317-abbd-4b4a-a38d-adb20f374e57",
        "title": "20% off Cycling Accessories at Halfords!",
        "description": "You can never be short of the right accessories, that is why Halfords has a huge range from lights to clothing and bike locks to helmets. There is something to suit all your needs.",
        "picture_url": "http://www.eetapp.com/uploads/stores/2604/halfords.jpg",
        "threshold": 0,
        "reactivation_time": 1440,
        "redemption_format": "code",
        "redemption_code": "P93F0N8E",
        "redemption_image_url": null,
        "terms_url": "http://blog.addthiscdn.com/wp-content/uploads/2017/06/22185645/test.jpg",
        "region": "All",
        "active": true,
        "tags": [],
        "created_at": "2018-05-08 11:36:57.000"
      }
    }
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