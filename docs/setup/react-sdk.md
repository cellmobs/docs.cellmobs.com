---
template: overrides/main.html
title: React SDK
---

# React SDK

Cellmobs provides a comprehensive Software Development Kit (SDK) designed for React.js and Next.js applications to ensure a smoother, faster development process. 
It is a [Next.js](https://nextjs.org/) project bootstrapped with [`create-next-app`](https://github.com/vercel/next.js/tree/canary/packages/create-next-app) which sets up the basic framework for developing Cellmobs clients using [React.js](https://reactjs.org/) and Next.js. 

Here are the main features of this SDK:

- **Pre-Built Components:**
The React SDK comes with a range of pre-built components that can be readily used in your application. These include components for authentication, form fields, data lists, page fragments. and various user interface elements. Using these pre-built components can significantly reduce development time and ensure consistency across your application.

- **Request Mapping Framework:**
The SDK includes a complete request mapping framework for the Cellmobs REST API and statement management through Redux. This framework provides simplified, promise-based methods for making requests to the API, abstracting the underlying HTTP methods. This means you don't need to manually craft HTTP requests or parse responses. 
For example, to fetch data from an endpoint, you can use the SDK's methods with simple parameters. The SDK handles the complexities of constructing the correct API call, sending it, and interpreting the response. 

- **Customizable and Extensible:**
While the SDK provides a lot of functionality out of the box, it's also designed to be customizable and extensible. You can extend the pre-built components or the request mapping framework to suit your specific needs. 


## Cloning the project
Before you get started, you need to install the following dependencies:

- [Git](https://github.com/git-guides/install-git){:target="_blank"} 
- [Node Js](https://docs.npmjs.com/downloading-and-installing-node-js-and-npm){:target="_blank"} 
- A suitable code editor (e.g. [Visual Studio Code](https://code.visualstudio.com/download){:target="_blank"})
- Access to [Github](https://github.com/cellmobs/cellmobs-react-sdk)

Once done, open a terminal and enter the following command
```bash
$ git clone https://github.com/cellmobs/cellmobs-react-sdk
$ cd cellmobs-react-sdk
```

## Getting Started

First , install the dependencies
```bash
# install dependencies
$ npm install
```
Next to run the development server:

```bash
$ npm run dev
# or
$ yarn dev
```

Open [http://localhost:3000](http://localhost:3000) with your browser to see the result.

You can start editing the page by modifying `pages/index.js`. The page auto-updates as you edit the file.

## Configuration

There is a `constants.js` file here you can edit the default API and ADMIN hosts.

```javascript

export const ENVIRONMENT = 'dev'
export const X_API_KEY = process.env.X_API_KEY || 'api-key'; // You Cellmobs API Key
export const X_TENANTID = process.env.X_TENANTID || 'tenant-id'; // Your Cellmobs Tenant ID
export const HOST_NAME = process.env.HOST_NAME || 'yourdomain.com';  // Your Application host
export const API_BASE_URL = process.env.API_BASE_URL || "https://app-name.web.cellmobs.com/v1"; // Your Cellmobs API host if app-name was the name of your app. 
export const CDN_BASE_URL = "https://cdn.cellmobs.com/";  // The Cellmobs public CDN 
export const ADMIN_BASE_URL = process.env.ADMIN_BASE_URL || "https://app-name.console.cellmobs.com";  // Your Cellmobs App Console host
export const RECAPTCHA_SITEKEY = process.env.RECAPTCHA_SITEKEY || "SITEKEY"; // Your Google re-CAPTCHA site key
export const GOOGLE_API_CLIENT_ID = process.env.GOOGLE_API_CLIENT_ID || ""; // Your Google API Client ID for Google Sign-In support
export const SUBSCRIPTION_PLAN_ID = process.env.SUBSCRIPTION_PLAN_ID || "646cb7c828a2997484c645e2"; // The Cellmobs Subscription your app will use (Optional)
export const GOOGLE_MEASUREMENT_ID = process.env.GOOGLE_MEASUREMENT_ID || "MEASUREMENTID";  // Your Google Analytics Measurement ID
export const TINY_MCE_KEY = process.env.TINY_MCE_KEY || "TINY-MCE-KEY";  // Your TinyMCE key in case you want to support inline editing

```

## Adding new pages
One of Next.js's best features is its support for a file-system-based router. This means that to create a new page, we

- Create a new folder with the name of the route in the pages directory
- Create an index.js file and add the React page component.
- Reference the new page in your existing pages.


## Deploy on Vercel
The easiest way to deploy your Next.js app is to use the [Vercel Platform](https://vercel.com/import?utm_medium=default-template&filter=next.js&utm_source=create-next-app&utm_campaign=create-next-app-readme) from the creators of Next.js.

Check out the [Next.js deployment documentation](https://nextjs.org/docs/deployment) for more details.

## Learn More
To learn more about Next.js, take a look at the following resources:

- [Next.js Documentation](https://nextjs.org/docs) - learn about Next.js features and API.
- [Learn Next.js](https://nextjs.org/learn) - an interactive Next.js tutorial.

You can check out [the Next.js GitHub repository](https://github.com/vercel/next.js/) - your feedback and contributions are welcome!


<br><br>