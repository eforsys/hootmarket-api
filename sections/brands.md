Brands
======

CRUD interface for Brands of Products.

Get Brands
----------

`GET /brands.json` returns all Brands.

**Optional Parameters**

* `sort={field}` specifies the order of the Brands.
* `sort_type={ASC | DESC}` specifies if sort is ascending (ASC) or descending (DESC). The default value is ASC. This parameter only work if the sort parameter is specified. 
* `per_page={number}` specifies the {number} of Brands returned by page. The default number is 100, maximum 200 and minimum 1.
* `page=#{number}` specifies the {number} of page to return.

**Response**

HTTP status 200 "ok" and the following json document in the body:

```
{
  data: [
    {
      id: 2,
      name: "Samsung",
      created_by_id: 1,
      created_at: "2013-06-26T20:48:53Z",
      updated_by_id: 1,
      updated_at: "2013-06-26T20:48:53Z"
    }, 
    ...
  ],
  pagination: {
    total_pages: 4,
    current_page: 1
  }
}
```
  
Get similar Brands
------------------

`GET /brands.json?q={term}` returns all similar Brands to {term}.

**Optional Parameters**

* `per_page={number}` specifies the {number} of Brands returned by page. The default number is 100, maximun 200 and minimun 1.
* `page=#{number}` specifies the {number} of page to return.

**Response**

HTTP status 200 "ok" and the following json document in the body:

```
{
  data: [
    {
      id: 2,
      name: "Samsung",
      created_by_id: 1,
      created_at: "2013-06-26T20:48:53Z",
      updated_by_id: 1,
      updated_at: "2013-06-26T20:48:53Z"
    }, 
    ...
  ],
  pagination: {
    total_pages: 4,
    current_page: 1
  }
}
```


Get Brand
---------

`GET /brands/{id}.json` returns a specific Brand with ID {id}.

**Response**

HTTP status 200 "ok" with the following json document:

```
{
  data: {
    id: 1,
    name: "Apple",
    created_by_id: 1,
    created_at: "2013-06-26T20:48:53Z",
    updated_by_id: 1,
    updated_at: "2013-06-26T20:48:53Z"
  }
}
```

Create Brand
------------

`POST /brands.json` creates a new Brand.

**Parameters**

* `name` Brand name.

**Response**

HTTP status 201 "created" with the following json document that contains the Brand created:

```
{
  data: {
    id: 1,
    name: "Apple",
    created_by_id: 1,
    created_at: "2013-06-26T20:48:53Z",
    updated_by_id: 1,
    updated_at: "2013-06-26T20:48:53Z"
  }
}
```

Update Brand
------------

`PATCH /brands{id}.json` updates a Brand specifies with ID {id}.

**Parameters**

* `name` Brand name.

**Response**

HTTP status 200 "ok" with the following json document that contains the Brand updated:

```
{
  data: {
    id: 1,
    name: "Apples",
    created_by_id: 1,
    created_at: "2013-06-26T20:48:53Z",
    updated_by_id: 1,
    updated_at: "2013-06-28T16:39:50Z"
  }
}
```

Delete Brand
------------

`DELETE /brands{id}.json` deletes a Brand specifies with ID {id}.

**Response**

HTTP status 200 "ok".
