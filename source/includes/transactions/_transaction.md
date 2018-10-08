# Transactions

## The Transaction Object

Parameter | Description
--------- | -----------
id | The unique identifier used by Portify for this transaction
made_on | The date the transaction was made (YYYY-MM-DD)
amount | The value of the transaction
currency | The currency that the transaction was made in
income | 'true' if the transaction was incoming to the account, 'false' if outgoing
description | Information about the transaction as it appears on their bank statement. Can be overwritten by the user
category | The category perscribed by our banking API or chosen by the user
custom | Whether the transaction was pulled from banking data (true) or added manually by the user (false)
selected | Whether the transaction has been marked as 'work related' by the user 
