Brands
======

CRUD interface for the brands of products.

Get brands
----------

* `GET /brands.json` returns all brands.

**Params**

* `limit=#{quantity}` limits the number of brands returned. The default quantity is 100, maximun 200 and minimun 1.
* `page=#{page_number}` specifies the page.
* `sort=(#{field} asc | #{field} desc)` specifies the order of brands.

**Response**

* HTTP status 200 "ok" and the following json document in the body:

  ``` json
  {
    brands: [
      {
        id: id,
        name: name
      }, 
      ...
    ],
    pagination: {
    }
  }
  ```

* HTTP status 200 "ok" with the following json document

Get brand
-----------
* `GET /brand/#{id}.json`

**Response**

``` json
{
  id: id,
  name: name
}
```

Get brand
-----------
* `GET /brand/#{id}.json`

