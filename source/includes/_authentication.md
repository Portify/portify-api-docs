# Authentication

Portify uses an Oauth2-style flow to authorize the sharing of data between user and Partner. The flow works as follows:

1) User taps button in Portify app that opens the Partner's 'landing_page_url'.

2) User taps a link on the Partner's landing page that takes them to https://www.portify.co/partner/applications/:APP_ID. An optional 'redirect_url' query string parameter can be passed, or the default one will be used.

3) The user signs in. On successful sign-in, a redirect is returned that sends the user to the Partner's desired redirect_url, with a temporary token as a query string parameter.

4) The Partner has up to 10 minutes to use the partner_integrations#create endpoint, that will convert the token to a non-expiring Partner Integration access_token. This access_token is used in all future requests to access information belonging to the user. This access_token does not expire, but can be revoked. 
