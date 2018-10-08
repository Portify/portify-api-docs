## [GET] Show a User

```shell
curl "ENV_URL/partners/users/:APP_ID"
  -X GET
  -H "Authorization": "Token token=SECRET"
  -H "Accept": "application/json"
  -H "Content-Type": "application/json"
```
> The above command returns JSON structured like this:

```json
{
  "user": {
    "name":"Chris Fairbank",
    "email":"chris@portify.co",
    "phone":"07234567890"
  }
}
```

This endpoint returns a the user associated with the given access token.

### Parameters

Parameter | Description
--------- | -----------
app_id | Your application's unique identifier [required]
