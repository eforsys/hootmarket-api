States
======

Get a list of all States for a Country, or get a specific State for a Country.

Get States
-------------

`GET /countries/{country_id}/states.json` returns all States into the Country with ID {country_id}.

The States will be sorted by name

**Response**

200 (ok) HTTP status and the following json document in the body:

> ```
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

Get similar States
------------------

`GET /countries/{country_id}/states.json?q={term}` returns all similar States to {term} and into the Country with ID {country_id}.

The States are sorted by similitude.

**Response**

200 (ok) HTTP status and the following json document in the body:

> ```
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

`GET /countries/{country_id}/states/{id}.json` returns a specific State withs Id {id} into the Country with Id {country_id}.

**Response**

200 (ok) HTTP status and the following json document in the body:

> ```
  {
    data: { 
      id: 3560,
      name: "Carlifornia",
      code: "CA",
      phone_code: "1"
    }
  }
  ```