# tasks API Spec

## Create tasks

Endpoint : POST /api/category/{idCategory}/tasks

Request Header :

- X-API-TOKEN : Token (Mandatory)

Request Body :

```json
{
  "title" : "Test",
  "description" : "Test Deskripsi"
}
```

Response Body (Success) :

```json
{
  "data" : {
    "id" : "randomstring",
    "title" : "Test",
    "description" : "Test Deskripsi"
  }
}
```

Response Body (Failed) :

```json
{
  "errors" : "Category is not found"
}
```

## Update tasks

Endpoint : PUT /api/category/{idCategory}/tasks/{idtasks}

Request Header :

- X-API-TOKEN : Token (Mandatory)

Request Body :

```json
{
    "title" : "Test Update",
    "description" : "Test Update Deskripsi"
}
```

Response Body (Success) :

```json
{
  "data" : {
    "id" : "randomstring",
    "title" : "Test Update",
    "description" : "Test Update Deskripsi"
  }
}
```

Response Body (Failed) :

```json
{
  "errors" : "tasks is not found"
}
```

## Get tasks

Endpoint : GET /api/category/{idCategory}/tasks/{idtasks}

Request Header :

- X-API-TOKEN : Token (Mandatory)

Response Body (Success) :

```json
{
  "data" : {
    "id" : "randomstring",
    "title" : "Test Update",
    "description" : "Test Update Deskripsi"
  }
}
```

Response Body (Failed) :

```json
{
  "errors" : "tasks is not found"
}
```

## Remove tasks

Endpoint : DELETE /api/category/{idCategory}/tasks/{idtasks}

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
  "errors" : "tasks is not found"
}
```

## List tasks

Endpoint : GET /api/category/{idCategory}/tasks

Request Header :

- X-API-TOKEN : Token (Mandatory)

Response Body (Success) :

```json
{
  "data": [
    {
      "id": "randomstring",
      "title" : "Test Update",
      "description" : "Test Update Deskripsi"
    }
  ]
}
```

Response Body (Failed) :

```json
{
  "errors" : "Category is not found"
}
```