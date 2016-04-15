###########################
Authenticating with Blitzen
###########################

Blitzen uses OAuth2.0 specification.  You must have an account within blitzen for it to work.

To start make an account if you haven't already at https://blitzen.com/signup

Once you have an account associated with blitzen, we can start the authorization flow.

Login with this url endpoint:
https://blitzen.com/api/v1/auth/login/

This will redirect you to our api portal.  If you're already logged in, the api portal is at this location:
https://blitzen.com/api/v1/o/applications/

Once the application is made, you can start the authentication flow from this authorization url:
https://blitzen.com/api/v1/o/token/


You can read more on authentication from django-oauth-toolkit from here: https://django-oauth-toolkit.readthedocs.org/en/latest/
