# Sessions

Allows to get authentication token for your GoFetch user account.

* [Create session](#create-session)
* [Destroy session](#destroy-session)

## Create session

`POST sessions`

Supply your GoFetch email and password to get your API authentication token. The token can then be used to authenticate other API requests. There is no need to supply `X-User-Email` or `X-User-Token` HTTP headers for this request.


### Request data

```JSON
{
  "email": "amanda.woo@hoverboard.net",
  "password": "Wa9nhCe@QFp"
}
```

Supply the `email` and `password` of your GoFetch user account.

### Response

```JSON
{ "authentication_token": "FSiWaVUP4oi0Bs9Ia9Xw" }
```

The returned authentication token is passed in the `X-User-Token` HTTP header to access other API endpoints. Authentication token will not change. The token needs to be stored securely.

### cURL example

```shell
curl -H 'Content-Type: application/json' \
  -d '{"email": "your@email.com", "password": "@9LFpShfE$yA"}' \
  http://test.go-fetch.com.au/public_api/v1/sessions
```


## Destroy session

`DELETE sessions`

Regenerates authentication token for your user account, which can be useful if you think your token escaped into the world. Returns an empty response. After the token has been regenerated, a new token can be obtained with [Create session](#create-session) request.

### cURL example

```shell
curl -X "DELETE" -H 'X-User-Email: EMAIL' -H 'X-User-Token: TOKEN' http://test.go-fetch.com.au/public_api/v1/sessions
```
