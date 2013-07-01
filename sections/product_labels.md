ProductLabels
======

CRUD interface for Labels of Products.

Get Labels
----------

`GET /product_labels.json` returns all Labels.

**Optional Parameters**

* `sort={field}` specifies the order of the Labels.
* `sort_type={ASC | DESC}` specifies if sort is ascending (ASC) or descending (DESC). The default value is ASC. This parameter only work if the sort parameter is specified. 
* `per_page={number}` specifies the {number} of Labels returned by page. The default number is 100, maximum 200 and minimum 1.
* `page=#{number}` specifies the {number} of page to return.

**Response**

HTTP status 200 "ok" and the following json document in the body:

```
{
  data: [
    {
      id: 2,
      name: "Summer Promotions 2013",
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
  
Get similar Labels
------------------

`GET /product_labels.json?q={term}` returns all similar Labels to {term}.

**Optional Parameters**

* `per_page={number}` specifies the {number} of Labels returned by page. The default number is 100, maximun 200 and minimun 1.
* `page=#{number}` specifies the {number} of page to return.

**Response**

HTTP status 200 "ok" and the following json document in the body:

```
{
  data: [
    {
      id: 2,
      name: "Summer Promotions 2013",
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


Get Label
---------

`GET /product_labels/{id}.json` returns a specific Label with ID {id}.

**Response**

HTTP status 200 "ok" with the following json document:

```
{
  data: {
    id: 1,
    name: "Winter Promotions 2013",  
    number_of_products: 18,  
    created_by_id: 1,
    created_at: "2013-06-26T20:48:53Z",
    updated_by_id: 1,
    updated_at: "2013-06-26T20:48:53Z"
  }
}
```

Create Label
------------

`POST /product_labels.json` creates a new Label.

**Parameters**

* `name` Label name.

**Response**

HTTP status 201 "created" with the following json document that contains the Label created:

```
{
  data: {
    id: 3,
    name: "Winter Promotions 2014",
    number_of_products: 0,
    created_by_id: 1,
    created_at: "2013-06-26T20:48:53Z",
    updated_by_id: 1,
    updated_at: "2013-06-26T20:48:53Z"
  }
}
```

Update Label
------------

`PATCH /product_labels{id}.json` updates a specific Label with ID {id}.

**Parameters**

* `name` Label name.

**Response**

HTTP status 200 "ok" with the following json document that contains the Label updated:

```
{
  data: {
    id: 3,
    name: "Winter Promotions 2014",
    number_of_products: 0,
    created_by_id: 1,
    created_at: "2013-06-26T20:48:53Z",
    updated_by_id: 1,
    updated_at: "2013-06-28T16:39:50Z"
  }
}
```

Delete Label
------------

`DELETE /product_labels{id}.json` deletes a specific Label with ID {id}.

**Response**

HTTP status 200 "ok".
