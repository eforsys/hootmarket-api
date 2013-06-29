Branches
======

CRUD interface for Branches of the Company.

Get Branches
----------

`GET /brands.json` returns all Branches.

**Optional Parameters**

* `sort={field}` specifies the order of the Branches.
* `sort_type={ASC | DESC}` specifies if sort is ascending (ASC) or descending (DESC). The default value is ASC. This parameter only work if the sort parameter is specified. 
* `per_page={number}` specifies the {number} of Branches returned by page. The default number is 100, maximum 200 and minimum 1.
* `page=#{number}` specifies the {number} of page to return.

**Response**

HTTP status 200 "ok" and the following json document in the body:

```
{
  data: [
    {
      id: 2,
      name: "New York 1020",
      address: "1020 Washington Street",
      zip_code: "10551",
      phone: "+1 210 636 3307",
      city_name: "New York City",
      created_by_id: 1,
      created_at: "2013-06-26T20:48:53Z",
      updated_by_id: 1,
      updated_at: "2013-06-26T20:48:53Z",
      country: {
      	id: 234,
      	name: "United Stated"
      },
      state: {
      	id: 3596,
      	name: "New York"
      },
      warehouses: [
      	{
      		id: 1,
      		name: "Main"
      	}
      	...
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
  
Get similar Branches
------------------

`GET /branches.json?q={term}` returns all similar Branches to {term}.

**Optional Parameters**

* `per_page={number}` specifies the {number} of Branches returned by page. The default number is 100, maximun 200 and minimun 1.
* `page=#{number}` specifies the {number} of page to return.

**Response**

HTTP status 200 "ok" and the following json document in the body:

```
{
  data: [
    {
      id: 2,
      name: "New York 1020",
      address: "1020 Washington Street",
      zip_code: "10551",
      phone: "+1 210 636 3307",
      city_name: "New York City",
      created_by_id: 1,
      created_at: "2013-06-26T20:48:53Z",
      updated_by_id: 1,
      updated_at: "2013-06-26T20:48:53Z",
      country: {
      	id: 234,
      	name: "United Stated"
      },
      state: {
      	id: 3596,
      	name: "New York"
      },
      warehouses: [
      	{
      		id: 1,
      		name: "Main"
      	}
      	...
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


Get Branch
---------

`GET /branches/{id}.json` returns a specific Branch with ID {id}.

**Response**

HTTP status 200 "ok" with the following json document:


```
{
  data: {
    id: 2,
    name: "New York 1020",
    address: "1020 Washington Street",
    zip_code: "10551",
    phone: "+1 210 636 3307",
    city_name: "New York City",
    created_by_id: 1,
    created_at: "2013-06-26T20:48:53Z",
    updated_by_id: 1,
    updated_at: "2013-06-26T20:48:53Z",
    country: {
      id: 234,
      name: "United Stated"
    },
    state: {
      id: 3596,
      name: "New York"
    },
    warehouses: [
      {
        id: 1,
      	name: "Main"
      }
      ...
    ]
  }
}
```

Create Branch
------------

`POST /branches.json` creates a new Branch.

**Parameters**

* `name` Branch name.
* `phone` Branch phone (optional)
* `zip_code` zip code where the Branch is located (optional)
* `city_name` city where the Branch is located
* `state_id` ID of the state where the Branch is located
* `country_id` ID of the country where the Branch is located

**Response**

HTTP status 201 "created" with the following json document that contains the Branch created:

```
{
  data: {
    id: 2,
    name: "New York 1020",
    address: "1020 Washington Street",
    zip_code: "10551",
    phone: "+1 210 636 3307",
    city_name: "New York City",
    created_by_id: 1,
    created_at: "2013-06-26T20:48:53Z",
    updated_by_id: 1,
    updated_at: "2013-06-26T20:48:53Z",
    country: {
      id: 234,
      name: "United Stated"
    },
    state: {
      id: 3596,
      name: "New York"
    },
    warehouses: [
      {
        id: 1,
        name: "Main"
      }
      ...
    ]
  }
}
```

Update Branch
------------

`PATCH /branches{id}.json` updates a Branch specifies with ID {id}.

**Parameters**

* `name` Branch name.
* `phone` Branch phone (optional)
* `zip_code` zip code where the Branch is located (optional)
* `city_name` city where the Branch is located
* `state_id` ID of the state where the Branch is located
* `country_id` ID of the country where the Branch is located

**Response**

HTTP status 200 "ok" with the following json document that contains the Branch updated:

```
{
  data: {
    id: 2,
    name: "New York 2020",
    address: "2020 Washington Street",
    zip_code: "10551",
    phone: "+1 210 636 3307",
    city_name: "New York City",
    created_by_id: 1,
    created_at: "2013-06-26T20:48:53Z",
    updated_by_id: 1,
    updated_at: "2013-06-28T16:39:50Z",
    country: {
      id: 234,
      name: "United Stated"
    },
    state: {
      id: 3596,
      name: "New York"
    },
    warehouses: [
      {
        id: 1,
        name: "Main"
      }
      ...
    ]
  }
}
```

Delete Branch
------------

`DELETE /branches{id}.json` deletes a Branch specifies with ID {id}.

**Response**

HTTP status 200 "ok".
