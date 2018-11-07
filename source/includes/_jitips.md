# Jitips

## Create a new Jitips


> POST **https://8enomg6g06.execute-api.eu-west-1.amazonaws.com/dev/tips**

```json
{
  "products": [
    {
      "id": "bc520f0a-686c-4ad0-9f62-8cda1dd046dc",
      "price": 29.35,
      "quantity": 2,
      "tax": 20
    },
    {
      "id": "8686c1dd046dc-686c-4686c-9f62-868686",
      "price": 5.78,
      "tax": 20
    }
  ],
  "tipser": {
    "email": "sted@nutshell-lab.com",
    "firstName": "Ted",
    "lastName": "Smith",
    "phone": "+33665000000",
    "dateOfBirth": "1995-12-17T03:24:00"
  },
  "metadata": {
    "orderId": "yourOwnId",
    "whatever": "youWant"
  }
}
```


To be created a jitips requires some information about the products bought (`products`) and the buyer (`tipser`). You might want to bind some extra data (like an order id) which you can do using `metadata` as a json object. 

__A product (item of `products`) as a json object should contain the following :__

field | required | type | Notes
-------|---------|------|--------
**id** | yes | GUID as string | Jitips GUID of the product.
**price** | yes | positive Number | Displayed price for bought product as of buying time.
**quantity** | no | positive Integer | Bought quantity for this product. Default : 1
**tax** | yes | Number between 0-100 | Tax to apply on price


__The `tipser` as a json object should contain the following :__

field | required | type | Notes
-------|---------|------|--------
**email** | yes | email as string | Buyer email.
**firstName** | yes | string(50) | Buyer first name.
**lastName** | no | string(50) | Buyer last name
**phone** | no | string(10-15)| Buyer phone
**dateOfBirth** | no | ISO date(YYYY-MM-DDTHH:mm:ss) as string | Buyer birth date

<aside class="warning">
If your customer bought the same product twice, you must not request a jitips with two <b>products</b>. You have to use <b>quantity</b> field instead.
</aside>

## Permalink

Once a Jitips has been created, it is tagged with a shortid and a permalink. Using this permaling anyone can join the jitips. The permalink is expected to redirect to your website.

## Join an existing Jitips

> POST **https://8enomg6g06.execute-api.eu-west-1.amazonaws.com/dev/tips/join**

```json
{
  "tips": ["BJyy7m8fEM", "S1x1CeTG4f", "BkeddpQ0LM"],
  "products": [
    {
      "id": "bc520f0a-686c-4ad0-9f62-8cda1dd046dc",
      "price": 29.35,
      "quantity": 2,
      "tax": 20
    },
    {
      "id": "8686c1dd046dc-686c-4686c-9f62-868686",
      "price": 5.78,
      "tax": 20
    }
  ],
  "tipser": {
    "email": "sted@nutshell-lab.com",
    "firstName": "Ted",
    "lastName": "Smith",
    "phone": "+33665000000",
    "dateOfBirth": "1995-12-17T03:24:00"
  },
  "metadata": {
    "orderId": "yourOwnId",
    "whatever": "youWant"
  }
}
```

So as to join an existing Jitips, you have to know which jitips your customer want to join. To do this you can use our permalink system. Here is what your are expecting to send to jitips API when you try to join one or many jitips :

__A product (item of `products`) as a json object should contain the following :__

field | required | type | Notes
-------|---------|------|--------
**id** | yes | GUID as string | Jitips GUID of the product.
**price** | yes | positive Number | Displayed price for bought product as of buying time.
**quantity** | no | positive Integer | Bought quantity for this product. Default : 1
**tax** | yes | Number between 0-100 | Tax to apply on price

__The `tipser` as a json object should contain the following :__

field | required | type | Notes
-------|---------|------|--------
**email** | yes | email as string | Joiner email.
**firstName** | yes | string(50) | Joiner first name.
**lastName** | no | string(50) | Joiner last name
**phone** | no | string(10-15)| Joiner phone
**dateOfBirth** | no | ISO date(YYYY-MM-DDTHH:mm:ss) as string | Joiner birth date

__The `tips` as a json array should contain shortIds as string.

<aside class="notice">
Alike the jitips creation, you might want to add extra data in <b>metadata</b> optional field as a json object.
</aside>

## Get all information about a jitips

> GET **https://8enomg6g06.execute-api.eu-west-1.amazonaws.com/dev/tips/:shortId**

field | required | type | Notes
-------|---------|------|--------
**shortId** | yes | Shortid as string | Shortid of the jitips.

<aside class="warning">
  <b>Not implemented yet! Coming soon.</b>
</aside>

## Get joinable product of a jitips

> GET **https://8enomg6g06.execute-api.eu-west-1.amazonaws.com/dev/tips/:shortId/allowed-products**

So as to join properly, you have to know with what product your customer can join a jitips. That's what this url can be used for.

<aside class="warning">
  <b>Not implemented yet! Coming soon.</b>
</aside>
