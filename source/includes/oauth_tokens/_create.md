# Oauth Tokens

## [POST] Create an Oauth Token

```shell
curl "ENV_URL/partners/oauth_tokens"
  -X POST
  -H "Authorization": "Token token=SECRET"
  -H "Accept": "application/json"
  -H "Content-Type": "application/json"
  -d '{
		"app_id": "APP_ID",
		"user_id": "906188c9-7bb1-4502-b882-fa207aafb1c6"
	}'
```
> The above command returns JSON structured like this:

```json
{
  "oauth_token": {
    "token":"IHOnuYHap_EDgoS3hBrxcyNoGzH7a5jTyhf4onUw1IU",
    "expires_at":"2018-10-04T15:46:57.833Z"
  }
}
```

This endpoint creates a new Oauth Token, that will be valid for 10 minutes.

### Parameters

Parameter | Description
--------- | -----------
app_id | Your app ID
user_id | The ID of the Portify user who wishes to share their data
