## [POST] Create a Custom Perk

```shell
curl "http://portify-api.herokuapp.com/companies/:company_id/admins/:admin_id/custom_perks"
  -X POST
  -H "Authorization": "Token token=yourtoken"
  -H "Accept": "application/json"
  -H "Content-Type": "application/json"
  -d '{
    "custom_perk": {
		  "title": "20% off Cycling Accessories at Halfords!",
		  "description": "You can never be short of the right accessories, that is why Halfords has a huge range from lights to clothing and bike locks to helmets. There is something to suit all your needs.",
		  "picture_url": "http://www.eetapp.com/uploads/stores/2604/halfords.jpg",
		  "threshold": 0,
		  "reactivation_time": 1440,
		  "redemption_format": "code",
		  "redemption_code": "P93F0N8E",
		  "redemption_image_url": nil,
		  "terms_url": "http://blog.addthiscdn.com/wp-content/uploads/2017/06/22185645/test.jpg",
		  "region": "All",
		  "active": true,
		  "tags": []
		}
	}'
```

> The above command returns JSON structured like this:

```json
{
	"custom_perk": {
	  "id": "906188c9-7bb1-4502-b882-fa207aafb1c6",
	  "title": "20% off Cycling Accessories at Halfords!",
	  "description": "You can never be short of the right accessories, that is why Halfords has a huge range from lights to clothing and bike locks to helmets. There is something to suit all your needs.",
	  "picture_url": "http://www.eetapp.com/uploads/stores/2604/halfords.jpg",
	  "threshold": 500,
	  "reactivation_time": 43200,
	  "redemption_format": "code",
	  "redemption_code": "P93F0N8E",
	  "redemption_image_url": null,
	  "terms_url": "http://blog.addthiscdn.com/wp-content/uploads/2017/06/22185645/test.jpg",
	  "region": "All",
	  "active": true,
	  "tags": [],
	  "created_at": "2018-05-08 11:36:57.000"
	},
	"message": { 
		"type": "success", 
		"text": "Perk Created Successfully!", 
		"code": "perk_create_success" 
	}
}
```

This endpoint creates a new custom perk.

### URL Parameters

Parameter | Description
--------- | -----------
company_id | The ID of your company
admin_id | The ID of your admin account
