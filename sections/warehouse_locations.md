Warehouse Locations
======

Query interface for Locations of the Warehouses.

Get Locations
----------

`GET /warehouses/{warehouse_id}/locations.json` returns all locations of a specified Warehouse {warehouse_id}.

**Optional Parameters**

* `sort={field}` specifies the order of the Locations.
* `sort_type={ASC | DESC}` specifies if sort is ascending (ASC) or descending (DESC). The default value is ASC. This parameter only work if the sort parameter is specified. 
* `per_page={number}` specifies the {number} of Locations returned by page. The default number is 100, maximum 200 and minimum 1.
* `page=#{number}` specifies the {number} of page to return.

**Response**

HTTP status 200 "ok" and the following json document in the body:

```
{
  data: [
    {
      name: "Box 1",
      created_by_id: 1,
      warehouse_id: 1
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
  
Get similar Locations
------------------

`GET /warehouses/{warehouse_id}/locations.json?q={term}` returns all similar Locations to {term} of a specified Warehouse.

**Optional Parameters**

* `per_page={number}` specifies the {number} of Locations returned by page. The default number is 100, maximun 200 and minimun 1.
* `page=#{number}` specifies the {number} of page to return.

**Response**

HTTP status 200 "ok" and the following json document in the body:

```
{
  data: [
    {
      name: "Box 1",
      created_by_id: 1,
      warehouse_id: 1
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
Get Location
---------

`GET /warehouses/{warehouse_id}/locations/{id}.json` returns a specific Location with ID {id} of a specified Warehouse {warehouse_id}.

**Response**

HTTP status 200 "ok" with the following json document:

```
{
  data: {
    name: "Box 1",
    created_by_id: 1,
    warehouse_id: 1
    created_at: "2013-06-26T20:48:53Z",
    updated_by_id: 1,
    updated_at: "2013-06-26T20:48:53Z"
  }
}
```
