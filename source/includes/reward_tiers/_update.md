## [PATCH] Update a Reward Tier

```shell
curl "http://portify-api.herokuapp.com/companies/:company_id/admins/:admin_id/reward_tiers/:id"
  -X PATCH
  -H "Authorization": "Token token=yourtoken"
  -H "Accept": "application/json"
  -H "Content-Type": "application/json"
  -d '{
		"reward_tier": {
		 	"name": "Sushi,
	  	"threshold": 500
		}
	}'
```

> The above command returns JSON structured like this:

```json
{
	"reward_tier": {
		"id": "28559585-8f21-410f-982e-419927db2276",
		"name": "Sushi",
		"threshold": 500,
		"flair_url": "https://emojipedia-us.s3.amazonaws.com/thumbs/240/apple/118/sushi_1f363.png"
	},
	"message": { 
		"type": "success", 
		"text": "Reward Tier Updated Successfully!", 
		"code": "reward_tier_update_success" 
	}
}
```

This endpoint updates a specific reward tier, overwriting attributes specified in the body of the request.

### URL Parameters

Parameter | Description
--------- | -----------
company_id | The ID of your company
admin_id | The ID of your admin account
id | The ID of the reward tier
