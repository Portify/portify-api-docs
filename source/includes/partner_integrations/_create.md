# Partner Integrations

## [POST] Create a Partner Integration

```shell
curl "ENV_URL/partners/integrations"
  -X POST
  -H "Authorization": "Token token=SECRET"
  -H "Accept": "application/json"
  -H "Content-Type": "application/json"
  -d '{
		"token": OAUTH_TOKEN
	}'
```
> The above command returns JSON structured like this:

```json
{
  "partner_integration": {
    "access_token":"IHOnuYHap_EDgoS3hBrxcyNoGzH7a5jTyhf4onUw1IU"
  }
}
```

This endpoint creates a new Partner Integration - between a Portify User and a Partner Application - and exposes a long-lasting access_token for requests against the user going forward.

### Parameters

Parameter | Description
--------- | -----------
token | The Oauth Token returned from the Portify sign-in page
