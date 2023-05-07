---
template: overrides/main.html
title: Pages
---

# Pages

Pages are the primary entity for configuring and managing web page templates, metadata, and content. They are encapsulated within the Cellmobs `WebPage` entity, which serves as the foundation for creating and organizing the structure of a web application.

WebPage entities allow developers to define the layout, design, and components of a web page, ensuring consistency and ease of management across the entire application. By using a WebPage entity, developers can create various types of pages, such as landing pages, blog posts, product pages, and more, all while maintaining a uniform look and feel.

Metadata associated with WebPage entities plays a crucial role in search engine optimization ([SEO](/guide/seo)) and accessibility. Developers can specify metadata such as title, description, keywords, and other relevant information to optimize their pages for search engines and provide a better user experience.

Content within a WebPage entity is flexible and can include text, images, videos, and other multimedia elements, enabling developers to create rich and engaging web pages that cater to their specific needs and target audience. WebPage content can be static or dynamic and fetched from the database and dynamically rendered through page ]template](/app-console/manage-templates/#web-) fragments. 


## Primary Content

## HTML Editor

## Request

## Template

## Metadata

## A/B Testing


As the organizational administrator, you hold the power to manage the application’s pages which were already created i.e., enable/disable a page to show up in the application.

For example : If a user wants to enable a new login page for their website (which was already created) 

  
___
## Managing Pages

- Go to [Pages Section](https://console.cellmobs.com/admin/pages/list)
- Click on Add Page 
- Enter the name of the “Page Meta Title”  
- Select the Status as Approved 
- Enter the hostname as “dev.cellmobs.com” (the company website) 
- Enter the path as “/login”  
- In the Right-side screen enter the name of the page that was created I.e., login (it will auto suggest the page name if it was already an existing page 
- Select the login 
- User will see the page UI after the selection 
- User can go back to his website and see if the login page is showing up  
- If user wants to disable this page
    - Go to manage users section  
    - Select the page that was created 
    - And change the status! = Approved 
    - Now, go back to the website and see if the login page is not showing up 

    <figure markdown>
[![Admin Pages]][Admin Pages]
    </figure>

[Admin Pages]: ../assets/screenshots/admin/admin-pages.png
