## [PATCH] Update a Partner Application

```shell
curl "ENV_URL/partners/integrations"
  -X PATCH
  -H "Authorization": "Token token=SECRET"
  -H "Accept": "application/json"
  -H "Content-Type": "application/json"
  -d '{
    "app_id": APP_ID,
    "partner_application": {
      "landing_page":"https://www.facebook.com",
      "logo_url":"https://image.shutterstock.com/image-photo/valencia-spain-march-05-2017-260nw-593204357.jpg"
    }
  }'
```
> The above command returns JSON structured like this:

```json
{
  "partner_application":
    {
      "name":"Google",
      "app_id":"D6wQE1hgo4dGx6FPkfRUzwu6",
      "landing_page_url":"https://www.facebook.com",
      "redirect_url":"https://www.google.com/callback_url",
      "logo_url":"https://image.shutterstock.com/image-photo/valencia-spain-march-05-2017-260nw-593204357.jpg",
      "active":true
    }
}
```

This endpoint updates a Partner Application. Not all fields are updateable, refer to the table below to learn which ones are. 

### Parameters

Parameter | Description
--------- | -----------
app_id | Your application's unique identifier [required]
name | Your application's name (visible on authorization page)
landing_page_url | Where you want Portify users to land when they want to access your application from the Portify app
logo_url | A URL to your application's logo (visible on authorization page)
redirect_url | Your default redirect_url when a user authorizes your application to access their data


