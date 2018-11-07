# Products

## Get all jitipsable products

> GET **https://8enomg6g06.execute-api.eu-west-1.amazonaws.com/dev/products**

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

## Get one jitipsable product


> GET **https://8enomg6g06.execute-api.eu-west-1.amazonaws.com/dev/products/:id**

field | required | type | Notes
-------|---------|------|--------
id | yes | GUID as string | Jitips GUID of the product

## Remove one jitipsable product


> DELETE **https://8enomg6g06.execute-api.eu-west-1.amazonaws.com/dev/products/:id**

field | required | type | Notes
-------|---------|------|--------
id | yes | GUID as string | Jitips GUID of the product

## Update one jitipsable product


> PUT **https://8enomg6g06.execute-api.eu-west-1.amazonaws.com/dev/products/:id**

```json
{
  "name": "Hivernal cereals",
  "description": "Lorem ipsum dolor sit amet.",
  "image": "https://url-over-ssl-are-better",
  "url": "https://path-to-your-product-details",
}
```

field | required | type | Notes
-------|---------|------|--------
id | yes | GUID as string | Jitips GUID of the product
name | yes | String(255) | Name of your product
description | yes | String(2000) | String description
image | no | Url | Url of a picture of your product
url | no | Url | Url of your product page

## Make a product jitipsable

> POST  **https://8enomg6g06.execute-api.eu-west-1.amazonaws.com/dev/products**

```json
{
  "name": "Hivernal cereals",
  "description": "Lorem ipsum dolor sit amet.",
  "image": "https://url-over-ssl-are-better",
  "url": "https://path-to-your-product-details",
}
```

field | required | type | Notes
-------|---------|------|--------
name | yes | String(255) | Name of your product
description | yes | String(2000) | String description
image | no | Url | Url of a picture of your product
url | no | Url | Url of your product page