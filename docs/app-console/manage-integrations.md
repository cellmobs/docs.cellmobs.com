---
template: overrides/main.html
title: Integrations
---

# Integrations

Cellmobs offers extensive API integration capabilities that empower developers to connect their applications with a wide range of popular cloud apps. 

For a quick introduction on Integrations and overview on how to obtain API credentials, please checkout [Setting Up Integrations](/setup/setting-up-integrations) 

This section will walk you through configuring Integrations in detail using the Cellmobs App Console. We use  [Dropbox](https://www.dropbox.com/developers){:target=_blank} as an example.  

## Configure an Integration

## Identity Connections

## Webhooks

Webhooks are an incredibly useful feature provided by many APIs, including those used by Cellmobs, to allow real-time communication between different applications. In essence, a webhook is a way for an app to provide other applications with real-time information. A webhook delivers data to other applications as it happens, meaning you get data immediately.

Many of Cellmobs' API integrations, such as Dropbox, support webhooks. These integrations allow your Cellmobs app to react to events that happen on the integrated application. For instance, if you have integrated your app with Jira, you can configure webhooks to notify your Cellmobs app when a ticket is updated or deleted in Jira.

The way it works is that each Cellmobs app has a dedicated webhook endpoint that can receive these notifications. When an event occurs on the external application, it sends a message to the webhook URL configured in Cellmobs. The message will typically contain information about the event, like what the event is and data associated with the event.

These webhooks are critical for keeping your application data in sync with the external applications you have integrated with. For instance, if a file is deleted in Dropbox, a webhook can notify your Cellmobs app of this event, and your app can then update its own data accordingly.

Moreover, webhooks can be connected to trigger Cellmobs [workflows](/setup/setting-up-workflow/). This means that when certain events occur on the external application, not only is your data kept in sync, but it can also trigger specific actions within your Cellmobs app, like sending an email, updating a database, or starting a marketing campaign. This makes webhooks a powerful tool for automating processes and keeping data consistent across different applications.

[WALKTHROUGH]

## Supported Integrations

We currently support the following integrations and are adding new ones every week. Please be sure to check back frequently or learn more about use our Zapier integration to utilize APIs we currently do not support.  


| API | Entity Types | Process Types | Status |
|------------|------------|--------------|-------------|
| Dropbox | `CONTENT` | `CREATE`, `SAVE`, `DELETE`, `MOVE`, `LIST` | Live | 
| OneDrive | `CONTENT` | `CREATE`, `SAVE`, `DELETE`, `MOVE`, `LIST` | Live | 
| Google Drive | `CONTENT` | `CREATE`, `SAVE`, `DELETE`, `MOVE`, `LIST` | Live | 
| BOX | `CONTENT` | `CREATE`, `SAVE`, `DELETE`, `MOVE`, `LIST` | Live | 
| AWS S3 | `CONTENT` | `CREATE`, `SAVE`, `DELETE`, `MOVE`, `LIST` | Live | 
| MS Contacts | `IDENTITY`, `ORGANIZATION` | `CREATE`, `SAVE`, `DELETE`, `MOVE`, `LIST` | Live | 
| MS Calendar | `CALENDAR_EVENT` | `CREATE`, `SAVE`, `DELETE`, `MOVE`, `LIST` | Live | 
| Hubspot  | `IDENTITY`, `ORGANIZATION`, `DEAL_TERMS`, `WORK`, `LEAD` | `CREATE`, `SAVE`, `DELETE`, `MOVE`, `LIST` | Live | 
| Google People | `IDENTITY`, `ORGANIZATION` | `CREATE`, `SAVE`, `DELETE`, `MOVE`, `LIST` | Live | 
| Google Calendar | `CALENDAR_EVENT` | `CREATE`, `SAVE`, `DELETE`, `MOVE`, `LIST` | Live | 
| MS Teams | `INBOX_ITEM`,`IDENTITY`, `ORGANIZATION` | `CREATE`, `SAVE`, `DELETE`, `MOVE` | Live | 
| Slack | `INBOX_ITEM`, `IDENTITY`,, `ORGANIZATION` | `CREATE`, `SAVE`, `DELETE`, `MOVE` | Live | 
| Mailchimp | `IDENTITY` | `CREATE`, `SAVE`, `DELETE`, `LIST` | Live | 
| Trello | `IDENTITY`, `PROJECT`, `WORK`  | `CREATE`, `SAVE`, `DELETE`, `LIST` | Live | 
| Jira | `IDENTITY`, `PROJECT`, `WORK`  | `CREATE`, `SAVE`, `DELETE`, `LIST` | Live | 
| Zapier | All entities  | `CREATE`, `SAVE`, `DELETE` | Live | 
| OpenAI | `WEB_PAGE`, `CONTENT`  | Generate Text and Images  | Live | 
| YouTube | `CONTENT`  | `CREATE`, `SAVE`, `DELETE`, `LIST` | Live | 

<br><br>