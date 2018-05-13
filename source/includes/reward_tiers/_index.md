# Reward Tiers

## [GET] Get All Reward Tiers

```shell
curl "http://portify-api.herokuapp.com/companies/:company_id/admins/:admin_id/reward_tiers"
  -H "Authorization": "Token token=yourtoken"
```

> The above command returns JSON structured like this:

```json
{
  "reward_tiers": [
    {
      "id": "28559585-8f21-410f-982e-419927db2276",
      "name": "Sushi",
      "threshold": 500,
      "flair_url": "https://emojipedia-us.s3.amazonaws.com/thumbs/240/apple/118/sushi_1f363.png"
    },
    {
      "id": "e60f875c-821e-4093-a376-70471e355766",
      "name": "Watermelon",
      "threshold": 250,
      "flair_url": "https://emojipedia-us.s3.amazonaws.com/thumbs/240/apple/118/watermelon_1f363.png"
    }
  ]
}
```

This endpoint retrieves all reward tiers.

### URL Parameters

Parameter | Description
--------- | -----------
company_id | The ID of your company
admin_id | The ID of your admin account