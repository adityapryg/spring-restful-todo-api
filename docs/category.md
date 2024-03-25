# category API Spec

## Create category

Endpoint : POST /api/categories

Request Header :

- X-API-TOKEN : Token (Mandatory)

Request Body :

```json
{
  "category" : "Education"
}
```

Response Body (Success) : 

```json
{
  "data": {
    "id" : "random-string",
    "category": "category",
  }
}
```

Response Body (Failed) :

```json
{
  "errors" : "Category format invalid, ..."
}
```

## Update category

Endpoint : PUT /api/categories/{idcategory}

Request Header :

- X-API-TOKEN : Token (Mandatory)

Request Body :

```json
{
  "category" : "Education"
}
```

Response Body (Success) :

```json
{
  "data": {
    "id" : "random-string",
    "firstName": "Education"
  }
}
```

Response Body (Failed) :

```json
{
  "errors" : "Category format invalid, ..."
}
```

## Get category

Endpoint : GET /api/categories/{idcategory}

Request Header :

- X-API-TOKEN : Token (Mandatory)

Response Body (Success) :

```json
{
  "data": {
    "id" : "random-string",
    "category": "Education",
  }
}
```

Response Body (Failed, 404) :

```json
{
  "errors" : "category is not found"
}
```

## Search category

Endpoint : GET /api/categories

Query Param :

- name : String, category's name

Request Header :

- X-API-TOKEN : Token (Mandatory)

Response Body (Success) :

```json
{
  "data": [
    {
      "id": "random-string",
      "category": "Education"
    }
  ],
  "paging" : {
    "currentPage" : 0,
    "totalPage" : 10,
    "size" : 10
  }
}
```

Response Body (Failed) :

```json
{
  "errors" : "Unauthorized"
}
```

## Remove category

Endpoint : DELETE /api/categories/{idcategory}

Request Header :

- X-API-TOKEN : Token (Mandatory)

Response Body (Success) :

```json
{
  "data" : "OK"
}
```

Response Body (Failed) :

```json
{
  "errors" : "category is not found"
}
```