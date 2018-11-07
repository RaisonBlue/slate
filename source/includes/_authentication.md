# Authentication

## Prerequisite

> [Register as a Jitips partner](https://app.jitips.com/partners/auth/signup?to=%2Fpartners%2F)

> [Get a developer Jitips Partner account](https://jitips.nutshell.ovh/partners/auth/signup?to=%2Fpartners%2F)


In order to be able to call Jitips API endpoints, you must have a Jitips Partner account. To get one, please sign up on [app.jitips.com](https://app.jitips.com/partners/auth/signup?to=%2Fpartners%2F). You will also need an API Key. Currently, you have to get in touch with us to get one.

<aside class="notice">
  <b>If you are a developer working with Jitips</b>, please register on <a href="https://jitips.nutshell.ovh/partners/auth/signup?to=%2Fpartners%2F">Nutshell servers</a> instead and ask Nutshell an api key to access to their test environements.
</aside>


## How to make an authenticated request

> ANY **https://8enomg6g06.execute-api.eu-west-1.amazonaws.com/dev/**

```json
  {
    "x-api-key": "meowmeowmeow"
  }
```

Stupid and simple, you just need to include your apiKey in your requests' headers. Besides authenticating you, the apiKey is also bound to your partner account and identify all of your requests.
