---
template: overrides/main.html
title: Creating Apps
---

# Creating Apps

The Cellmobs platform is designed to enable customers to develop and manage multiple apps, each with its own unique environment and set of resources. Here's how it works:

## Create a New App
Once you're logged into your Cellmobs account, you can easily create a new application through the "Your Apps" section user interface. This involves naming your application, and optionally providing a description to help you remember its purpose.

## Tenant ID Assignment 
Every new application is assigned a unique tenant ID. This serves as an identifier that helps to separate the data and operations of one application from another. It's crucial for maintaining the isolation and integrity of each application's data and operations.

## API Credentials
Once your new application is created, you can generates [API keys](/guide/authentication/#api-key) for it. These API keys are used to authenticate your application when it communicates with the Cellmobs platform, ensuring that only authorized applications can interact with your app's data and functionality.

## Dedicated Database
Each application on Cellmobs has its own dedicated [MongoDB](/technologies/#mongodb) database. This means your application's data is stored separately from other applications, ensuring data privacy and security. Also, this architecture enables each application to scale its database resources independently based on its specific requirements.

<br><br>