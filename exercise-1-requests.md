Requests

## Create a user

```json
{
 "id": 0,
 "firstName": "Fire",
 "username": "firedonkey",
 "lastName": "Donkey",
 "email": "firedonkey@petsandthings.com",
 "password": "donkeypong",
 "phone": "12345678",
 "userStatus": 0
}
```

cURL
```
curl -X POST --header 'Content-Type: application/json' --header 'Accept: application/json' -d '{ \
  "id": 0, \
  "firstName": "Fire", \
  "username": "firedonkey", \
  "lastName": "Donkey", \
  "email": "firedonkey%40petsandthings.com", \
  "password": "donkeypong", \
  "phone": "12345678", \
  "userStatus": 0 \
 } \
 ' 'http://petstore.swagger.io/v2/user'
```

Request URL
`http://petstore.swagger.io/v2/user`

Response code: 200

Response headers
```
{
  "access-control-allow-origin": "*",
  "date": "Sun, 27 Nov 2016 15:23:57 GMT",
  "server": "Jetty(9.2.9.v20150224)",
  "connection": "close",
  "access-control-allow-headers": "Content-Type, api_key, Authorization",
  "access-control-allow-methods": "GET, POST, DELETE, PUT",
  "content-type": "application/json"
}
```

## Retrieve a user

cURL

```
curl -X GET --header 'Accept: application/xml' 'http://petstore.swagger.io/v2/user/firedonkey'
```

Request URL
```
http://petstore.swagger.io/v2/user/firedonkey
```

Response body
```xml
<?xml version="1.0" encoding="UTF-8" standalone="yes"?>
<User>
  <email>firedonkey@petsandthings.com</email>
  <firstName>Fire</firstName>
  <id>0</id>
  <lastName>Donkey</lastName>
  <password>donkeypong</password>
  <phone>12345678</phone>
  <userStatus>0</userStatus>
  <username>firedonkey</username>
</User>
```

Response headers
```
{
  "access-control-allow-origin": "*",
  "date": "Sun, 27 Nov 2016 15:28:58 GMT",
  "server": "Jetty(9.2.9.v20150224)",
  "connection": "close",
  "access-control-allow-headers": "Content-Type, api_key, Authorization",
  "access-control-allow-methods": "GET, POST, DELETE, PUT",
  "content-type": "application/xml"
}
```

## Update your user

Request body
```
{
  "id": 0,
  "username": "firedonkey",
  "firstName": "Fire",
  "lastName": "Donkey",
  "email": "firedonkey@petsandthings.com",
  "password": "ponogopoly",
  "phone": "12345678",
  "userStatus": 0
}
```

cURL
```
curl -X PUT --header 'Content-Type: application/json' --header 'Accept: application/json' -d '{ \
   "id": 0, \
   "username": "firedonkey", \
   "firstName": "Fire", \
   "lastName": "Donkey", \
   "email": "firedonkey%40petsandthings.com", \
   "password": "ponogopoly", \
   "phone": "12345678", \
   "userStatus": 0 \
 }' 'http://petstore.swagger.io/v2/user/firedonkey'
 ```

 ## Remove your user

 cURL
 ```
 curl -X DELETE --header 'Accept: application/json' 'http://petstore.swagger.io/v2/user/firedonkey'
 ```
