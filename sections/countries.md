Countries
=========

Get a list of all Countries, search or get a specific Country.

Get Countries
-------------

`GET /countries.json` returns all Countries.

The Countries are sorted by name.

**Response**

200 (ok) HTTP status and the following json document in the body:

```
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

Get similar Countries
---------------------

`GET /countries.json?q={term}` returns all similar Countries to {term}.

The Countries are sorted by similitude.

**Response**

200 (ok) HTTP status and the following json document in the body:

```
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

`GET /countries/{id}.json` returns a specific Country with ID {id}.

**Response**

200 (ok) HTTP status and the following json document in the body:

```
{
  data: { 
    id: 234,
    name: "United States",
    code: "US",
    phone_code: "1"
  }
}
```