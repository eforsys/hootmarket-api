Countries
=========

Get a list of all Countries, or get a specific Country.

Get Countries
-------------

`GET /countries.json` returns all Countries.

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

`GET /country/#{id}.json` returns a specific Country with the Id.

**Response**

200 (ok) HTTP status and the following json document in the body:

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