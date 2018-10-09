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
  "partner_application": {
    "name":"Google",
    "app_id":"D6wQE1hgo4dGx6FPkfRUzwu6",
    "landing_page_url":"https://www.facebook.com",
    "redirect_url":"https://www.google.com/callback_url",
    "redirect_url_host":"www.google.com",
    "logo_url":"https://image.shutterstock.com/image-photo/valencia-spain-march-05-2017-260nw-593204357.jpg",
    "active":true
  }
}
```

This endpoint updates a Partner Application. The following fields are not updateable via API request: 'app_id', 'active', 'redirect_url_host'.
