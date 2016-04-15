# Authenticating with Blitzen

Blitzen uses OAuth2.0 specification.  You must have an account within blitzen for it to work.

## Create Account

To start make an account if you haven't already at [https://blitzen.com/signup](https://blitzen.com/signup)

## Login

Login with this url endpoint:
[https://blitzen.com/api/v1/auth/login/](https://blitzen.com/api/v1/auth/login/)

## Create Oauth Client Application
This will redirect you to our api portal.  If you're already logged in, the api portal is at this location:
[https://blitzen.com/api/v1/o/applications/](https://blitzen.com/api/v1/o/applications/)

Set the `Client Type` to `public`

Set the `Authorization Grant Type` to `password`

A redirect URI is optional.

## Obtaining an access token

Once the application is made, you can start the authentication flow from this authorization url:
`https://blitzen.com/api/v1/o/token/`

### Access token request using cURL:

#### Example post:
```shell
$ curl -X POST -d "client_id=HJZ12WYAlG32DxXFyvD1ACgPgcdkg9E4DpcYFImOZ&amp;client_secret=ACja8bh12fsjFhVOEX8B3flcGsdfI77mao0zi55DgtrN4RGGmD5RQVMkw48TYhTOew33wSKiZ4W6dnqJoqE2nR2GbDxsejYUZ9wM389T6y7b7bORpOKI2Igl3c9w8zBDDpG&amp;grant_type=password&amp;username=someuser@gmail.com&amp;password=somepassword" http://localhost:8000/api/v1/o/token/
```

#### Example response:
```shell
{
  "refresh_token": "tp8zs1Ivc2mPkkYaHJ5ZHr6NP8wEOj", 
  "token_type": "Bearer", 
  "access_token": "SL2EOuq21Ac1xtjjZUTLPNqa5xsWmF", 
  "expires_in": 36000, 
  "scope": "read forms write"
}
```


You can read more on authentication from django-oauth-toolkit from here: https://django-oauth-toolkit.readthedocs.org/en/latest/
