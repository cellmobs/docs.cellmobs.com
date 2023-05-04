---
template: overrides/main.html
---

# Setting up Integrations

Cellmobs offers extensive API integration capabilities that empower developers to connect their applications with a wide range of popular cloud apps. For most integrations, Cellmobs supports the [OAuth2 Authorization Code Grant Flow](https://oauth.net/2/grant-types/authorization-code/){:target="_blank"}, a secure and reliable authentication mechanism that grants your application access to resources and data of users who authorize your application to access their information on the external service.

The OAuth2 Authorization Code Grant Flow has several benefits:

- **Enhanced security**: This flow provides a high level of security, as it relies on a temporary authorization code that is exchanged for an access token, minimizing the risk of token exposure.

- **Fine-grained permissions**: OAuth2 allows users to grant your application specific permissions, ensuring that your app has only the necessary access to their data on the external service.

- **Refresh tokens**: This flow supports refresh tokens, enabling your application to maintain long-lived access to a user's data without requiring the user to re-authenticate frequently.

- **User consent**: Users must explicitly authorize your application to access their data, ensuring that they maintain control over their information.

For non-OAuth integrations, Cellmobs typically relies on a simple API key and secret or access token to authorize your app to make requests against the external API (e.g., AWS S3). This approach simplifies the authentication process while still providing a reasonable level of security as Cellmobs encrypts API credentials at rest, in transit, and through added field level encryption.

By offering various API integration options, Cellmobs enables developers to build powerful and flexible applications that seamlessly connect with the tools and services their users already know and trust.

## OAuth2 APIs

The Cellmobs API offers [dedicated OAuth2 endpoints](https://api.cellmobs.com/#cb1e0d32-e42c-4181-9874-bdaa64f2b3de){:target="_blank"} to facilitate seamless integration with external cloud applications using OAuth2. These endpoints handle critical aspects of the OAuth2 process, making it easier for developers to implement secure and efficient integrations.

Configuring an OAuth2 integration involves a few key steps to ensure a smooth connection between your Cellmobs application and the desired cloud application. 

1. **Register with the cloud application's developer network:** Sign up for a developer account on the platform you want to integrate with (e.g. [Google](https://console.cloud.google.com/){:target="_blank"}, [Hubspot](https://developers.hubspot.com/){:target="_blank"}, [Dropbox](https://www.dropbox.com/developers){:target=_blank}, etc.). This will give you access to their API and developer resources.

2. **Configure an app with the proper scope and permissions for the APIs of that cloud application:** Create a new application within the developer network and specify the required OAuth2 scopes and permissions to access the necessary APIs. The scope determines the level of access your application will have, and permissions define the specific actions your application can perform.

3. **Add the OAuth2 client credentials to your Cellmobs application:** Once you have created your application and obtained your client ID and client secret, enter these credentials into your Cellmobs app's [integration settings](/app-console/manage-integrations). This will allow you or your Cellmobs app users authenticate with the cloud application using OAuth2.

4. **Implement the OAuth2 authorization flow in your Cellmobs app:** The Cellmobs API exposes dedicated OAuth2 endpoints for both generating an Authorization Url and to receive the OAuth2 callback to exchange the code with a valid access token. Depending on the use case and your app's requirements, you might need to allow users to trigger the authorization flow in your app and configure the integration accordingly. Once configured, Cellmobs API integrations will:
    1. **Generate an Authorization URL**: Cellmobs API provides an endpoint to generate an OAuth2 authorization URL. When a user wants to authorize your application to access their data on the external cloud application, they will be redirected to this authorization URL. The user will then log in to their account on the external service and grant your application the necessary permissions.
    2. **Receive OAuth2 Callback and Exchange Authorization Code for Access Token**: Once the user authorizes your application, the external cloud application will redirect them back to your application, including an authorization code in the callback URL. The Cellmobs API provides a dedicated endpoint to handle this callback and exchange the authorization code for an access token. This access token allows your application to make authorized API requests on behalf of the user.
    3. **Manage Access Tokens and Refresh Tokens**: The Cellmobs API takes care of managing access tokens and refresh tokens for each integration. It ensures that access tokens are securely stored and refreshed as needed, so your application can continue to make API requests without interruptions.

5. **Configure optional webhooks to receive event notifications from the cloud application:** If the cloud application supports webhooks, you can configure them to notify your Cellmobs app when specific events occur (e.g., a new contact is created in Hubspot). Webhooks enable real-time communication between the cloud application and your Cellmobs app, allowing you to react to events and synchronize data between the two systems.

By following these steps, you can successfully integrate your Cellmobs application with various cloud applications using OAuth2, unlocking powerful features and functionality for your users.

Click here to learn how to [configure Integrations](/app-console/manage-integrations).



<br><br>