# Selected Income

## [GET] List Selected Income

```shell
curl "ENV_URL/partners/selected_expenses?access_token=ACCESS_TOKEN&from_date=2018-06-01&to_date=2018-10-03"
  -X GET
  -H "Authorization": "Token token=SECRET"
  -H "Accept": "application/json"
  -H "Content-Type": "application/json"
```
> The above command returns JSON structured like this:

```json
{
  "selected_income":[
    {
      "id":"0ddb0af6-4e39-4512-ba31-2b4a3683e928",
      "made_on":"2018-06-08",
      "amount":"22.50",
      "currency":"GBP",
      "income":true,
      "description":"MILROY'S OF SOHO",
      "category":"Alcohol and Bars",
      "custom":false,
      "selected":true
    },
    {
      "id":"239a2549-00ae-44ec-b740-ac01a0482d41",
      "made_on":"2018-06-15",
      "amount":"144.53",
      "currency":"GBP",
      "income":true,
      "description":"BUTCHER OAF",
      "category":"Income (General)",
      "custom":false,
      "selected":true
    },
    {
      "id":"e96c7a93-9081-4543-9c56-a72ed738941c",
      "made_on":"2018-06-25",
      "amount":"1.07",
      "currency":"GBP",
      "income":true,
      "description":"ITUNES.COM/BILL",
      "category":"Transfer",
      "custom":false,
      "selected":true
    },
    ...
  ]
}
```

This endpoint returns an array of all <a href="#transactions">transactions</a> within the given timeframe that are marked as work-related income.

### Parameters

Parameter | Description
--------- | -----------
access_token | Your access token for the user you wish to get data for
from_date | String representing the date you want to receive transactions from (YYYY-MM-DD)
to_date | String representing the date you want to receive transactions until (YYYY-MM-DD)
