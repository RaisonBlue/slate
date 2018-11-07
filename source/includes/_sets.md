# Sets

## Create a set

> POST **https://8enomg6g06.execute-api.eu-west-1.amazonaws.com/dev/sets**

```json
{
  "duration": 86400,
  "enabled": false,
  "productIds": [
    "bc520f0a-686c-4ad0-9f62-8cda1dd046dc",
    "8686c1dd046dc-686c-4686c-9f62-868686",
    "bcd0466a-d0466c-4ad0-9f62-8d046dd46dc"
  ]
}
```

As a partner you're able to create Set. A set gather your products as a jitipsable group, this means that a product within your set will be jitipsable with any other product of the same set. A set have extra property :

field | required | type | Notes
-------|---------|------|--------
**duration** | yes | seconds as integer | Jitips' duration
**maxDiscount** | yes | percentage as number | Jitips' max Discount
**enabled** | No | Boolean | enable/disable the jitips (default: true)
**productsIds** | No | Array of GUID as string | A list of allowed product's GUID (default: [])


## Get all sets

> GET **https://8enomg6g06.execute-api.eu-west-1.amazonaws.com/dev/sets**

```json
{
  "page": 3,
  "per_page": 15
}
```

field | required | type | Notes
-------|---------|------|--------
page | yes | Integer | The page you want to acess
per_page | yes | Integer | Element per page

## Get one set

> GET **https://8enomg6g06.execute-api.eu-west-1.amazonaws.com/dev/sets/:id**

field | required | type | Notes
-------|---------|------|--------
id | yes | GUID as string | Jitips GUID of the set


## Update one set


> PATCH **https://8enomg6g06.execute-api.eu-west-1.amazonaws.com/dev/sets/:id**


```json
{
  "duration": 86400,
  "enabled": false,
  "productIds": [
    "bc520f0a-686c-4ad0-9f62-8cda1dd046dc",
    "8686c1dd046dc-686c-4686c-9f62-868686",
    "bcd0466a-d0466c-4ad0-9f62-8d046dd46dc"
  ]
}

```

field | required | type | Notes
-------|---------|------|--------
**id** | yes | GUID as string | Jitips GUID of the set
**duration** | yes | seconds as integer | Jitips' duration
**maxDiscount** | yes | percentage as number | Jitips' max Discount
**enabled** | No | Boolean | enable/disable the jitips (default: true)
**productsIds** | No | Array of GUID as string | A list of allowed product's GUID (default: [])



## Remove one set


> DELETE **https://8enomg6g06.execute-api.eu-west-1.amazonaws.com/dev/sets/:id**

field | required | type | Notes
-------|---------|------|--------
id | yes | GUID as string | Jitips GUID of the set
