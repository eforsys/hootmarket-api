Errors
======

This section contains the list of commons errors returned by this API.

HTTP 404 record not found
-------------------------

Returned when a specified record is not found.

By Example:

> `GET /countries/999.json`
  
> The country with the Id 999 not exists, therefore the 404 (not found) 
  HTTP status error, and the following json document in the body, is returned:

> ```
  {
    errors: [
      "There is not a Country with the Id 999"
    ]
  }
  ```
