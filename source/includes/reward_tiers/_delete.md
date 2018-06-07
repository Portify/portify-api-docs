## [DELETE] Delete a Specific Reward Tier

```shell
curl "http://portify-api.herokuapp.com/companies/:company_id/admins/:admin_id/reward_tiers/:id"
  -X DELETE
  -H "Authorization": "Token token=yourtoken"
```

> The above command returns JSON structured like this:

```json
{
  "id": "28559585-8f21-410f-982e-419927db2276",
	"message": { 
		"type": "success", 
		"text": "Reward Tier Deleted Successfully!", 
		"code": "reward_tier_delete_success" 
	}
}
```

This endpoint deletes a reward tier.

### URL Parameters

Parameter | Description
--------- | -----------
company_id | The ID of your company
admin_id | The ID of your admin account
id | The ID of the reward tier to delete


