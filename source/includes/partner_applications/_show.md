## [GET] Show a Partner Application

```shell
curl "ENV_URL/partners/applications/:APP_ID"
  -X GET
  -H "Accept": "application/json"
  -H "Content-Type": "application/json"
```
> The above command returns JSON structured like this:

```json
{
  "partner_application": {
    "name":"Google",
    "app_id":"D6wQE1hgo4dGx6FPkfRUzwu6",
    "landing_page_url":"https://www.google.com",
    "redirect_url":"https://www.google.com/callback_url",
    "logo_url":"http://assets.media-marketing.com/wp-content/uploads/2017/11/zasto-je-google-ov-logo-nesavrseno-savrsen.jpg",
    "active":true
  }
}
```

This endpoint returns an existing Partner Application. SECRET token is not required to use this endpoint. 

### Parameters

Parameter | Description
--------- | -----------
app_id | Your application's unique identifier [required]
