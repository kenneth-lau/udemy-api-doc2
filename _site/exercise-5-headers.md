# Exercise 5: Documenting headers

## FantasticFoto

`POST https://phantasticfoto/api/v1/`

Header Name | Description | Required | Notes
--- | --- | --- | ---
Content-Type | Format of the photo | Optional | Valid values: image/jpeg, image/png, and image/gif. Default is image/jpeg
Accept | Format of the returned data | Optional | Valid values: application/json and application/xml. Default is application/json

### Sample request

Request to upload a JPEG photo and return data in XML format.

```
POST https://phantasticfoto/api/v1/
Content-Type: image/jpeg
Accept: application/xml
```

POST body is the image to upload.
