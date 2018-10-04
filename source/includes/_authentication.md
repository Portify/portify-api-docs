# Authentication

Portify uses an Oauth2-style flow to authorize the sharing of data between user and Partner. The flow works as follows:

1) User taps button in Portify app that opens the Partner's 'redirect_url'. The user_id is passed as a query parameter.

2) The Partner captures the user_id and generates a token using the Oauth_Tokens#create endpoint. The partner redirects the user to https://www.portify.co/partner_applications/:APP_ID?token=1234.

3) The user has up to 10 minutes to sign-in on this page before the token expires.

4) If sign-in is successful, user is redirected to the Partner's 'callback_url' with a partner_integration token passed as a query string parameter. This token can be used by the Partner to authenticate requests against the user going forward. It does not expire but can be revoked.