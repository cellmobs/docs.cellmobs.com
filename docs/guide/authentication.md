---
template: overrides/main.html
title: Authentication
---

# Authentication

The Cellmobs API security is designed to provide robust protection and ensure the integrity of all API requests. To achieve this, the platform employs a two-fold security mechanism that requires both a valid API Key and a valid JSON Web Token (JWT) to be passed with each API request.

## API Key

The API Key is a unique identifier that is associated with your account or application. To authenticate your API requests, you must include the API Key as a password in the 'x-api-key' header. This key serves as a primary layer of authentication, verifying that the request is coming from a legitimate source with the necessary credentials to access the API.

## JWT Token

In addition to thes API Key, the Cellmobs API security also requires a valid JWT token for each request. The JWT token is a compact, URL-safe means of representing claims to be transferred between two parties. You need to pass the JWT token in the 'Authorization' header of the API request as `Bearer` token. The token ensures that the user making the request has the appropriate permissions and validates their identity.

## How to Authenticate

By employing this two-fold security mechanism, the Cellmobs API ensures that only authorized users with the correct credentials can access and interact with the platform's resources. 

#### Step 1: Create an API Key

To create an API Key go the [Apps Section](https://dev.cellmobs.com/apps){:target="_blank"} and choose the app for which you want to generate a new key. If you don't have an app yet we suggest you consult our [Quickstart Guide](/setup/quickstart).

<figure markdown>
![Configure Organization Roles](/assets/guide/generate-api-key.png){loading=lazy}
    <figcaption>Apps: Active API Keys</figcaption>
</figure>



#### Step 2: Authenticate to get a valid JWT Token

To obtain a JWT token simply [Login](https://api.cellmobs.com/#f42c872d-7c67-4db3-976c-889963ea979d){:target="_blank"} with an active application user.  

You can use our [postman collection](/guide/using-postman) or try the [API sandbox](/guide/api-sandbox). 

``` py title="Login"
curl --location 
--request POST 'https://web.cellmobs.com/v1/auth/login?username={email}&password={password}' \
--header 'x-api-key: my-api-key'

```


## Rate Limiting

Cellmobs employs a rate limiting mechanism using token bucket allocation to manage and control the rate at which API requests are processed for each app. This method helps maintain the stability and performance of the platform, ensuring a consistent and reliable experience for our customers and their users.

By default, each app is allocated 1,000 tokens per minute, meaning that it can make up to 1,000 API requests within a 60-second window. The token bucket allocation operates on a rolling basis, replenishing tokens at a constant rate, and allowing unused tokens to carry over to the next minute, up to the maximum limit.

If the default allocation of 1,000 tokens per minute is not sufficient for your app's needs, you can request an increase in your token limit by [opening a support ticket](https://www.cellmobs.com/support). Our support team will evaluate your request and, if approved, increase the token allocation to better accommodate your app's requirements.

This approach to rate limiting ensures fair resource usage among all apps on the Cellmobs platform while providing the flexibility for subscribers to request adjustments based on their specific needs.

----