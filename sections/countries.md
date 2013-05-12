Countries
=========

The countries API allows get list of all countries.

Get Countries
-------------

`GET /countries.json` returns all countries.

**Response**

200 (ok) HTTP status and the following json document in the body:

> ``` json
  {
    data: [
      {
        id: 239,
        name: "Venezuela",
        code: "VE",
        phone_code: "58"
      },
      ...
    ]
  }
  ```

Get Country
-----------

`GET /country/#{id}.json`

**Response**

> ``` json
  {
    data: { 
      id: 234,
      name: "United States",
      code: "US",
      phone_code: "1"
    }
  }
  ```