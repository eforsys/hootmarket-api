Warehouses
======

Query interface for Warehouses of the Branches.

Get Warehouses
----------

`GET /warehouses.json` returns all Warehouses.

**Optional Parameters**

* `sort={field}` specifies the order of the Warehouses.
* `sort_type={ASC | DESC}` specifies if sort is ascending (ASC) or descending (DESC). The default value is ASC. This parameter only work if the sort parameter is specified. 
* `per_page={number}` specifies the {number} of Warehouses returned by page. The default number is 100, maximum 200 and minimum 1.
* `page=#{number}` specifies the {number} of page to return.

**Response**

HTTP status 200 "ok" and the following json document in the body:

```
{
  data: [
    {
      name: "NY 1020",
      created_by_id: 1,
      created_at: "2013-06-26T20:48:53Z",
      updated_by_id: 1,
      updated_at: "2013-06-26T20:48:53Z",
      branch: {
        id: 2,
        name: "New York 1020",
        address: "1020 Washington Street",
        zip_code: "10551",
        phone: "+1 210 636 3307",
        city_name: "New York City",
        country: {
          id: 234,
      	 name: "United Stated"
        },
        state: {
      	 id: 3596,
      	 name: "New York"
        }
      },
      locations: [
        {
          name: Box 1
        }
      ]
    }, 
    ...
  ],
  pagination: {
    total_pages: 4,
    current_page: 1
  }
}
```
  
Get similar Warehouses
------------------

`GET /warehouses.json?q={term}` returns all similar Warehouses to {term}.

**Optional Parameters**

* `per_page={number}` specifies the {number} of Warehouses returned by page. The default number is 100, maximun 200 and minimun 1.
* `page=#{number}` specifies the {number} of page to return.

**Response**

HTTP status 200 "ok" and the following json document in the body:

```
{
  data: [
    {
      name: "NY 1020",
      created_by_id: 1,
      created_at: "2013-06-26T20:48:53Z",
      updated_by_id: 1,
      updated_at: "2013-06-26T20:48:53Z",
      branch: {
        id: 2,
        name: "New York 1020",
        address: "1020 Washington Street",
        zip_code: "10551",
        phone: "+1 210 636 3307",
        city_name: "New York City",
        country: {
          id: 234,
      	 name: "United Stated"
        },
        state: {
      	 id: 3596,
      	 name: "New York"
        }
      },
      locations: [
        {
          name: Box 1
        }
      ]
    }, 
    ...
  ],
  pagination: {
    total_pages: 4,
    current_page: 1
  }
}
```

Get Warehouse
---------

`GET /warehouses/{id}.json` returns a specific Warehouse with ID {id}.

**Response**

HTTP status 200 "ok" with the following json document:

```
{
  data: {
    name: "NY 1020",
    created_by_id: 1,
    created_at: "2013-06-26T20:48:53Z",
    updated_by_id: 1,
    updated_at: "2013-06-26T20:48:53Z",
    branch: {
      id: 2,
      name: "New York 1020",
      address: "1020 Washington Street",
      zip_code: "10551",
      phone: "+1 210 636 3307",
      city_name: "New York City",
      country: {
        id: 234,
        name: "United Stated"
      },
      state: {
        id: 3596,
        name: "New York"
      }
    },
    locations: [
      {
         name: "Box 1"
      }
    ]
  }
}
```

Update Warehouse
------------

`PATCH /warehouses{id}.json` updates a specific Warehouse with ID {id}.

**Parameters**

* `name` Warehouse name.

**Response**

HTTP status 200 "ok" with the following json document that contains the Warehouse updated:

```
{
  data: {
    name: "Warehouse New York 1020",
    created_by_id: 1,
    created_at: "2013-06-26T20:48:53Z",
    updated_by_id: 1,
    updated_at: "2013-06-28T16:39:50Z",
    branch: {
      id: 2,
      name: "New York 1020",
      address: "1020 Washington Street",
      zip_code: "10551",
      phone: "+1 210 636 3307",
      city_name: "New York City",
      country: {
        id: 234,
        name: "United Stated"
      },
      state: {
        id: 3596,
        name: "New York"
      }
    },
    locations: [
      {
         name: "Box 1"
      }
    ]
  }
}
```


