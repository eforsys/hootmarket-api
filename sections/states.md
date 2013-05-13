States
======

Get a list of all States for a Country, or get a specific State for a Country.

Get States
-------------

`GET /countries/#{country_id}/states.json` returns all States int the Country with the Country_id.

**Response**

200 (ok) HTTP status and the following json document in the body:

> ``` json
  {
    data: [
      {
        id: 3531,
        name: "Florida",
        code: "FL",
        country_id: "234"
      },
      ...
    ]
  }
  ```

Get Country
-----------

`GET /countries/#{country_id}/states/#{id}.json` returns a specific State with the Id into the Country with the Country_id.

**Response**

200 (ok) HTTP status and the following json document in the body:

> ``` json
  {
    data: { 
      id: 3560,
      name: "Carlifornia",
      code: "CA",
      phone_code: "1"
    }
  }
  ```