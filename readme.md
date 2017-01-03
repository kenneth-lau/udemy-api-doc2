# Notes from the "Learn API Technical Writing 2: REST for Writers" course
For more information, see [Learn API Technical Writing 2: REST for Writers] (https://www.udemy.com/learn-api-technical-writing-2-rest-for-writers/) at Udemy.

## Exercises
- Exercise 1: [Requests](exercise-1-requests.md)
- Exercise 2: [Methods](exercise-2-methodandurl.md)
- Exercise 3: [Using query parameters](exercise-3-queryparameters.md)
- Exercise 4: [Documenting query parameters](exercise-4-queryparameters.md)
- Exercise 5: [Headers](exercise-5-headers.md)
- Exercise 6: [Status codes](exercise-6-statuscodes.md)
- Exercise 7: [Reference doc](exercise-7-reference.md)

## 1.2 REST
* REST: Design pattern not protocol
* Any data format
* Stateless - doesn't keep track of device's state on server
  * Handled by client

## 2.3 Requests
* REST Requests
 * Method: e.g. GET, POST, DELETE  
 * URL: http, https, server domain,
 * query parameters: in key/value pairs
 * headers: for specific types of data
  * data formats
  * authorization
* body: JSON/XML, media file
  * used when a significant amount of data
  * only for POST or put

## 2.4 Resources
* data concept
* resource defined in the URL
* URL contains singular nouns: e.g. restaurant, flights
* resource objects that exist have an ID
* endpoint: URL corresponding to a resource
* resources can be contained in other Resources

## 2.5 Methods
* CRUD - create, retrieve, update, delete
* GET - retrieves data, no body, use IDs in URL for particular resource
* POST - creates a new resource object, data in the body
* PUT - modifies an existing resource object, data in the body
* DELETE

## 2.8 Query parameters
* modify or filter data returned
* after the question mark in the URL
* key and value separated by = significant
* Examples: pagination, filter, format (usually in header)
* specifying format: header, query parameter, suffix
* authorization (usually uses header)
* documentation in a table
  * parameter, description, type, required, notes
* all values are technically strings
  * integer, date, URL

## 2.11 headers
* key/value pairs
* data format
  * Content-Type: application/json (request (POST or PUT))
  * Accept: application/json (response)
* authorization
  * Bearer
* table with: header name, description, (required), values

## 2.13 Authentication and authorization
* Security
* Authentication
  * valid username and password
  * results in return of an access token
* Authorization
  * you send the server an access token
  * access token determines what API requests you can make
* App keys
  * API keys
  * developer portal gives user an app keys
  * key is sent to the server for an access token
* OAuth
  * Most APIs use OAuth 2.0
  * different users have different privileges
  * each API user has an access token
  * tokens are temporary
  * one-legged
    * data that anyone can access
  * three-legged
    * user data to be protected
    * 3 pathways: client device, authentication server, API server
  * grant types
    * authorization code - server side applications
    * implicit - mobile, web applications
      * access token sent as query parameter in redirect URL from authentication server
* header
* documentation
  * "authorization" section
    * URL of the authentication server

## 2.14 Request bodies and responses
* Structured data
  * only POST and PUT
* URLs in responses
* "No response body is returned"
* Object section
  * If same objects repeat
* Errors
  * HTTP status codes
    * code and description
    * table with: code, description, notes
  * elements in the response body
    * document like other response elements

## 3.16 Putting it all togeter
* **USEFUL:** Templates

## 3.18 Tools for documentation
* single source tools
* content management systems
  * web-based
  * good for collaboration
* autogenerated documentation tools
* markdown
* making REST requests
  * REST client
