# Exercise 7: Reference documentation

## Uploading sound files

Uploads a sound file to the current user's profile

### URL endpoint

`POST https://api.sounddate.com/profile/sound`

### Headers

Header | Description | Required | Values
--- | --- | --- | ---
Bearer | Access token | Required | {access token}
Content-Type | Sound file format | Optional | Valid values: audio/mpeg for mp3, audio/xwav for wav. Default is audio/mpeg.
Accept | Response format | Optional | Valid values: application/xml, application/json. Default is application/json.

The POST body is the sound file.

Note: The sound file must be 5 minutes or shorter.

### Sample request

`POST https://api.sounddate.com/profile/sound`

Bearer: MDI4NzUzMTk5MDE0ODAzNDI2NDIxOWI4Ng000
Content-Type: audio/mpeg
Accept: application/json

### Response

Element | Description | Type | Notes
--- | --- | --- | ---
id | ID of the new sound file | sound file |
length | Length of the sound file | Length | Length in seconds

### Sample response

```json
{
   "id":123456789,
   "length":239
}
```

## Retrieving sound file information

Retrieves information for a sound file for a user

### URL endpoint

`GET  https://api.sounddate.com/user/{user id}/profile/sound.`

### Query parameters

Parameter | Description | Type | Required | Notes
--- | ---- | --- | --- | ---
sortOrder | Determines order that files are returned | Integer | Optional | Valid values: mostRecent, earliest, shortest, longest. Default is mostRecent

### Headers

Header | Description | Required | Values
--- | ---- | --- | ---
Bearer | Access token | String | {access token}
Accept | Response format | String | application/xml, application/json

### Sample request

```
GET
https://api.sounddate.com/user/345354/profile/sound?sortOrder=shortest
Bearer: {access token}
Accept: application/json
```

### Response

Element | Description | Type | Notes
--- | --- | --- | ---
soundFiles | List of sound file information | Array |
id | ID of the sound file | Integer |
url | URL of the sound file | string |
length | Length of the sound file | integer | Length in seconds


### Sample response

```json
{
 "soundFiles": [
 {
 "id": 23456,
 "url": "https://api.sounddate.com/profile/sound/23456.mp3",
 "length": 11.2
 },
 {
 "id": 24559,
 "url": "https://api.sounddate.com/profile/sound/24559.mp3",
 "length": 19.8
 }
 ]
}
```

### Status codes and errors

Code | Description | Notes
--- | --- | ---
200 | OK | Success
401 | Unauthorized | Access token invalid
413 | Payload Too Large | Sound file is too long
