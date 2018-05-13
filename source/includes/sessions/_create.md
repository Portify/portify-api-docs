# Sessions

## [POST] Create a Session

```shell
curl "http://portify-api.herokuapp.com/admins/sessions"
  -X POST
  -H "Accept": "application/json"
  -H "Content-Type": "application/json"
  -d '{
		"session": {
		  "email": "example@gmail.com",
		  "password": "macncheese"
		}
	}'
```

> The above command returns JSON structured like this:

```json
{
	"admin": {
		"id": "45904836-aace-44c2-b29a-e0a30eab7a4e",
		"company_id": "46e62bbe-f23d-4d4c-a362-cba36ddb506a",
		"name": "Chris Butcher",
		"email": "chris@portify.co"
	},
	"token": "miFW6zkY3V4BiVCUXofJhFfw"
}
```

This endpoint creates a new session. admin[id], admin[company_id], and token should be recorded to use in all future API calls. Token is regenerated every time this endpoint is successfully called. Tokens do not otherwise expire.
