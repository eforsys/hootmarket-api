ProductGroups
======

CRUD interface for Groups of Products.

Get Groups
----------

`GET /product_groups.json` returns all Groups.

**Optional Parameters**

* `sort={field}` specifies the order of the Groups.
* `sort_type={ASC | DESC}` specifies if sort is ascending (ASC) or descending (DESC). The default value is ASC. This parameter only work if the sort parameter is specified. 
* `per_page={number}` specifies the {number} of Groups returned by page. The default number is 100, maximum 200 and minimum 1.
* `page=#{number}` specifies the {number} of page to return.

**Response**

HTTP status 200 "ok" and the following json document in the body:

```
{
  data: [
    {
      id: 2,
      name: "Cellphones",
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
  
Get similar Groups
------------------

`GET /product_groups.json?q={term}` returns all similar Groups to {term}.

**Optional Parameters**

* `per_page={number}` specifies the {number} of Groups returned by page. The default number is 100, maximun 200 and minimun 1.
* `page=#{number}` specifies the {number} of page to return.

**Response**

HTTP status 200 "ok" and the following json document in the body:

```
{
  data: [
    {
      id: 2,
      name: "Cellphones",
      created_by_id: 1,
      created_at: "2013-06-26T20:48:53Z",
      updated_by_id: 1,
      updated_at: "2013-06-26T20:48:53Z"
    }, 
    ...
  ],
  pagination: {
    total_pages: 2,
    current_page: 1
  }
}
```


Get Group
---------

`GET /product_groups/{id}.json` returns a specific Group with ID {id}.

**Response**

HTTP status 200 "ok" with the following json document:

```
{
  data: {
    id: 1,
    name: "Accessories",  
    number_of_products: 80,  
    created_by_id: 1,
    created_at: "2013-06-26T20:48:53Z",
    updated_by_id: 1,
    updated_at: "2013-06-26T20:48:53Z"
  }
}
```

Create Group
------------

`POST /product_groups.json` creates a new Group.

**Parameters**

* `name` Group name.

**Response**

HTTP status 201 "created" with the following json document that contains the Group created:

```
{
  data: {
    id: 3,
    name: "Tablets",
    number_of_products: 0,
    created_by_id: 1,
    created_at: "2013-06-26T20:48:53Z",
    updated_by_id: 1,
    updated_at: "2013-06-26T20:48:53Z"
  }
}
```

Update Group
------------

`PATCH /product_groups{id}.json` updates a specific Group with ID {id}.

**Parameters**

* `name` Group name.

**Response**

HTTP status 200 "ok" with the following json document that contains the Group updated:

```
{
  data: {
    id: 3,
    name: "Tablets Accessories",
    number_of_products: 0,
    created_by_id: 1,
    created_at: "2013-06-26T20:48:53Z",
    updated_by_id: 1,
    updated_at: "2013-06-28T16:39:50Z"
  }
}
```

Delete Group
------------

`DELETE /product_groups{id}.json` deletes a specific Group with ID {id}.

**Response**

HTTP status 200 "ok".
