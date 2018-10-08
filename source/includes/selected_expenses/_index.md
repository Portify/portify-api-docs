## [GET] List Selected Expenses

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
  "selected_expenses": [
    {
      "id":"7d777719-8c2a-4ada-b82e-80d1604340a7",
      "made_on":"2018-06-06",
      "amount":"5.45",
      "currency":"GBP",
      "income":false,
      "description":"PAYPAL PAYMENT",
      "category":"Shopping (General)",
      "custom":false,
      "selected":true
    },
    {
      "id":"1c92660a-b4c6-4b37-8639-cc410e5b8f54",
      "made_on":"2018-06-07",
      "amount":"49.00",
      "currency":"GBP",
      "income":false,
      "description":"HelloFresh",
      "category":"Groceries",
      "custom":false,
      "selected":true
    },
    {
      "id":"40bd0712-7d59-4c44-b342-b3ab24be46e3",
      "made_on":"2018-06-15",
      "amount":"6.50",
      "currency":"GBP",
      "income":false,
      "description":"THE B STREET DELI",
      "category":"Transfer",
      "custom":false,
      "selected":true
    },
    ...
  ]
}
```

This endpoint returns an array of all <a href="#transactions">transactions</a> within the given timeframe that are marked as work-related expenses.

### Parameters

Parameter | Description
--------- | -----------
access_token | Your access token for the user you wish to get data for [required]
from_date | String representing the date you want to receive transactions from (YYYY-MM-DD) [required]
to_date | String representing the date you want to receive transactions until (YYYY-MM-DD) [required]
