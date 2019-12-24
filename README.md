This repo contains a set of 4 client-side JavaScript examples for logging users into your custom app with Okta:

* `okta_auth_sdk/oidc_token`: Uses the Okta Auth JS library to create an instance of `OktaAuth` to redirect to Okta for hosted login, and retrieve and store tokens from the authorization server.
* `okta_auth_sdk/session`:  Uses the Okta Auth JS library to submit a user's credentials via the Authn API, retrieve a session token, and exchange the session token for an id_token.
* `signin_widget/idp_disco`: Uses the Okta Sign In Widget configured for IdP discovery to authenticate a user. To see IdP discvoery in action you'll need an Identity Provider configuration with an appropriate routing rule in your Okta tenant.
* `signin_widget/social`: Uses the Okta Sign In Widget configured with a social login provider to authenticate. You'll need to configure a social login IdP in your Okta tenant.

To run them, after configuring your OIDC client, just change to the directory of the example you want to run and fire up an HTTP Server locally on port 8000, for example using Python:

    python -m SimpleHTTPServer

Then navigate to http://localhost:8000 in your browser and keep an eye on the console for log messages explaining what's happening.

TODO:

- Write a bash script populate configuration values from a `.env` file.
