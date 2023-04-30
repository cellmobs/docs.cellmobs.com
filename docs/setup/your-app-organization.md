---
template: overrides/main.html
title: Your App Organization
---

# Your App Organization

In the Cellmobs platform, each Tenant App is associated with a primary default Organization. This default Organization serves as the foundation for configuring the main settings of an app, ensuring that it operates according to the desired requirements.

When a new app is created, a new blank database is automatically generated for that app. This database includes the default app configuration, which can be customized to meet the specific needs of the app. Alongside the default app configuration, a sysadmin account is also created within the primary default Organization.

The system administrator account with `ROLE_SYSADMIN` is provisioned with the credentials of the primary Cellmobs customer account, granting the account holder full administrative access to the app and its associated settings. This enables the account holder to manage and modify the app configuration, user roles, permissions, and other essential aspects of the app as needed.

By utilizing a primary default Organization and sysadmin account, the Cellmobs platform simplifies the initial setup process and ensures a consistent and secure foundation for every Tenant App. This approach allows for a seamless transition from app creation to customization and ongoing management, providing a reliable and user-friendly experience for app developers and administrators.

## Settings 

In the Celmobs platform, Organization settings play a crucial role in configuring and managing various aspects of your application. These settings help define the appearance, behavior, and structure of your app and can be customized to suit your specific requirements. Some of the essential Organization settings include:

1. **Global System Property**: This setting establishes the application organization ID, which is referenced throughout the application. The organization ID serves as a unique identifier for the main organiztion of your app, allowing the platform to associate resources, user roles, and permissions with the correct organization.
2. **Image Settings**: Image settings define the default dimensions and MIME types for common application image FileTypes, such as organization logos, user avatars, product images, and web page images. By configuring these settings, you can ensure that images are displayed consistently and appropriately across your app, and on differen device types (Mobile, Desktop, or Tablets).
3. **Real World Locations**: This setting allows you to define the physical locations associated with your organization, such as offices, stores, with geofences, or warehouses. By specifying real-world locations, you can manage resources, inventory, and other location-specific data within your application.
4. **Organization Members**: Organization members settings enable you to manage the users associated with your organization. You can add, remove, or modify user roles and permissions, ensuring that each user has the appropriate level of access and functionality within the app.
5. **Processor Credentials**: Processor credentials settings allow you to configure the payment processing and authentication details for your application. These settings are essential for handling transactions, subscriptions, and other financial aspects of your app.
6. **Subscription Plans**: Subscription plan settings enable you to define and manage the various products, pricing tiers, features, and benefits associated with your application. By customizing these settings, you can create a range of subscription options tailored to the needs and preferences of your users.

<br>

## Use Cases 

Organizations in the Cellmobs platform are a flexible and versatile feature that can be employed in various contexts and for different use cases. They serve as a way to group and manage users, permissions, and resources, catering to the unique requirements of different business verticals and application scenarios. Some common contexts and use cases for Organizations include:

- **[Marketplaces](guide/marketplaces)**: In a marketplace setting, Organizations can represent different suppliers, buyers, or sellers. They facilitate the management of transactions, listings, and user interactions specific to each Organization, enabling a seamless and organized marketplace experience. 
- **[Communities](guide/communities)**: For community-based applications, Organizations can represent distinct user groups, clubs, or interest areas. They help manage discussions, content sharing, and user interactions within the community, fostering a sense of belonging and engagement.
- **[E-commerce](guide/e-commerce)**: In an e-commerce context, Organizations can denote various departments or teams within a company, such as marketing, sales, or customer support. This organizational structure allows for effective resource allocation and management across different aspects of the business.
- **Business Verticals**: Organizations can be tailored to suit the needs of different business verticals, such as finance, healthcare, or education. They enable the management of user roles, permissions, and resources specific to each industry, ensuring compliance with industry-specific regulations and requirements.
- **Partnerships:** Organizations can also represent business partners, affiliates, or collaborators. They provide a structured way to manage shared resources, data, and communications, fostering productive and organized collaborations.
- **User Groups:** In a company setting, Organizations can be used to represent different departments or teams. This structure enables effective communication, task management, and resource sharing among team members, promoting collaboration and efficiency within the company.

The flexibility and adaptability of Organizations within the Cellmobs platform enable you to tailor the feature to your specific application requirements and use cases. By leveraging Organizations, you can create a more organized, efficient, and user-friendly experience, ensuring that users can easily navigate and interact with the various aspects of your app.

<br><br>