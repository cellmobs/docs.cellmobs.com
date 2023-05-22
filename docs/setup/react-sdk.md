---
template: overrides/main.html
title: React SDK
---

# React SDK

Cellmobs provides a React SDK that allows us to easily build a UI for your application.

It is a [Next.js](https://nextjs.org/) project bootstrapped with [`create-next-app`](https://github.com/vercel/next.js/tree/canary/packages/create-next-app) which sets up the basic framework for developing Cellmobs clients using [React.js](https://reactjs.org/) and Next.js. 

## Cloning the project
Before we get started, we need to fulfill the following dependencies

- Git
- Node Js
- A suitable code editor (e.g. Visual Studio Code)
- Access to Bitbucket

Once done, open a terminal and enter the following command
```bash
$ git clone https://<USER>@bitbucket.org/cellmobs/cellmobs-react.git
$ cd cellmobs-react
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

export const API_BASE_URL = "https://dev.cellmobs.com/rest";
export const CDN_BASE_URL = "https://cdn.cellmobs.com/";
export const ADMIN_BASE_URL = "https://dev.cellmobs.com";
```
## Testing

There is currently an issue with axios accepting unsigned SSL certificates which makes local API connection difficult.
There are several workaround to make axios accept invalid certificates, but I haven't been able to make them work yet.

```javascript

axios.defaults.httpsAgent = new https.Agent({ rejectUnauthorized: true }); // Not working
```
Another option is to add the self-signed certificated of the local API host to your certificate store as described here:
https://nishabe.medium.com/how-to-add-ssl-cert-to-the-java-trust-store-bbd1a52940c2

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