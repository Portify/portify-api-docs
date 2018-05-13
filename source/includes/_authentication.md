# Authentication

The Portify API is quick to get started with.

1) Receive the email and password to your Admin account.

2) <a href="/#sessions">Create a Session</a>, and record the admin_id, company_id, and token.

3) Use the company_id and admin_id as required in the endpoint URLs. Use the token in the authorization header of your request.

<aside class="notice">
	Tokens do not expire, unless a new session is requested.
</aside>