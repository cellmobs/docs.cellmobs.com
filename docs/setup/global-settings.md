---
template: overrides/main.html
title: Global Settings
---

# Global Settings

This section explores the more important settings that impact the overall functionality, appearance, and behavior of your app on a global level. 

The list of settings is ever evolving so be sure to check back frequently. 

## Important App Settings

App Settings are managed using the [App Console](/app-console/other-settings). [:fontawesome-solid-table-columns:](/app-console/other-settings) 

| Method      | Description                          | Sample |
| ----------- | ------------------------------------ | ----------------------|
|`app.name`|The name of your app. | CELLMOBS | 
|`app.organization.id`|The MongoDB id of your primary organization| [:fontawesome-regular-circle-question:](/app-console/manage-organizations "Locate your organization id") | 
|`app.organization.ledger.id`| The id of the ledger used for recording app revenue and costs. | [:fontawesome-regular-circle-question:](/app-console/manage-organizations "Learn more about Ledgers") | 
|`application.domain`| The main domain of you application. | cellmobs.com | 
|`application.icon`| The url of your app favicon | /favicon.ico | 
|`application.icon.large`|| | 
|`application.logo`| The url of your app logo | <img alt="Logo" src="https://cdn.cellmobs.com/2029399/static/images/android-icon-48x48.png" style="height:32px;"> | 
|`application.logo.lite`| | | 
|`aws.default.region`|us-east-1| | 
|`aws.access.key`  | AWS Access Key for overriding the default App assets storage location | ######  | 
|`aws.secret.access.key` | Access Secret Access Key for overriding the default App storage location | ###### | 
|`cdn.bucket` | S3 bucket for public static assets | media.cellmobs.com  | 
|`cdn.host` | CDN host for public static assets |  https://cdn.cellmobs.com | 
|`cdn.root.folder`| S3 folder for public static assets | app-1/ | 
|`file.bucket`| S3 bucket for secure files | files.cellmobs.com | 
|`file.bucket.root`| S3 folder for secure files|  cellmobs-dev/|  
|`chatgpt.api.key`| Optional Open AI api key| sk-################## | 
|`contact-request-alert-recipients`| Optional comma-delimited list of email, that should receive contact request alert | [:fontawesome-regular-circle-question:](/app-console/manage-leads "Learn more about Leads")| 
|`facebook.app.id`| Your Facebook App ID associated with your app | 2156##########| | 
|`google.analytics.id`| Google Analytics Measurement ID | UA-#########-1|  
|`google.maps.key`| Google Map API Key | AIzaSyB6Q99Sf_#################| | 
|`google.tag.manager.id`| Google Tag Manager ID | GTM-N56ZFB6| | 
|`host.domain`| Your application host |  dev.cellmobs.com|  
|`messaging.from.email`| The email address that is used for sending application alerts | info@cellmobs.com| 
|`recaptcha.secret.key`| The Google reCAPTHCA secret key | [:fontawesome-regular-circle-question:](https://www.google.com/recaptcha/about/){:target="_blank"} | 
|`recaptcha.site.key`|The Google reCAPTHCA site key | [:fontawesome-regular-circle-question:](https://www.google.com/recaptcha/about/){:target="_blank"} | 
|`supported.languages`|es,es,fr,ru,it,zh,de| | 
|`twilio.account.sid`| The Twilio account sid for sending text messages | [:fontawesome-regular-circle-question:](/setup/message-templates/#text-message-templates) | 
|`twilio.auth.token`| The Twilio account auth token for sending text messages | [:fontawesome-regular-circle-question:](/setup/message-templates/#text-message-templates) | 
|`twilio.verify.sid`| The Twilio account verify sid |  [:fontawesome-regular-circle-question:](/setup/message-templates/#text-message-templates) | 

<br>
