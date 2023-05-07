---
template: overrides/main.html
title: Users
---

# Users

Users of your application are represented by the `Identity` entity. Each user is assigned a single [Global Role](/setup/security#global-roles) that determines their access level and permissions within the app. 

For customers or regular users, they are typically assigned the `ROLE_USER`. This role provides them with basic access to the application, allowing them to interact with the app's features and functionality in a limited capacity. If your application has more tiered access levels or requires additional permissions for certain users, you can configure these using [Organization Roles](/setup/security/#organization-roles), which offer more granular control over user permissions.

For team members who require elevated access to your application, such as developers, sales, or customer support teams, you should consider assigning a higher-level role. Some examples of these elevated roles include:

**`ROLE_EDITOR`**: This role allows users to create, edit, and manage content within the application, such as products, articles, or other content types.

**`ROLE_MANAGER`**: Users with this role have increased access to administrative functions, including managing user accounts, overseeing transactions, and monitoring application performance.

**`ROLE_ADMIN`**: The `ROLE_ADMIN` provides the highest level of access to the application, allowing users to manage all aspects of the app, including configuration, user management, and system settings.

Assigning appropriate roles to your users is crucial for maintaining the security and integrity of your application. It helps ensure that users have the necessary permissions to perform their tasks while preventing unauthorized access to sensitive information or critical app functions.

<br>

!!! info 
    Any role higher than `ROLE_USER` is considered a Team Member role and would impact the total number of users on your [Cellmobs Account](https://www.cellmobs.com/account). 

    For Identity data such as general contacts you can assign the role `ROLE_NONUSER`. This users with this role will be assigned a random passsword and will not be able to login until their role is elevated to at least `ROLE_USER`. 




As the administrator, you hold the power to to add, import, and invite users to join your users, as well as control the user's access rights and change the user's role and location. 

___

## Add Users

## Notifications

## Payment Options


We can invite users to the users. Invitations will be sent to the specified email addresses. They will be added to the users only based on their approval. 

- Go to the [Users Section](https://console.cellmobs.com/admin/users/list) 
- Click on Add user 
- Profile Tab:
    - Upload the image of the person (optional) 
    - Provide the required fields like “First Name”, “Last Name “, “Role”, “Phone Number” and other details like birth day, Address etc. (if necessary) 
- Account details Tab: 
    - Provide the details like user name, email address,  
    - You can also provide a few more details for Account security like, Login attempts, Login verification, Account status etc. 
- Change Password Tab:  
    - We can change or recover password 
- Notifications details:
    - We can modify the notification channels as desired by the user.

    <figure markdown>
[![Admin Users 1]][Admin Users 1]
    </figure>
    <figure markdown>
[![Admin Users 2]][Admin Users 2]
    </figure>
    <figure markdown>
[![Admin Users 3]][Admin Users 3]
    </figure>
    <figure markdown>
[![Admin Users 4]][Admin Users 4]
    </figure>
    <figure markdown>
[![Admin Users 5]][Admin Users 5]
    </figure>
    <figure markdown>

[Admin Users 1]: ../assets/screenshots/admin/admin-users-1.png
[Admin Users 2]: ../assets/screenshots/admin/admin-users-2.png
[Admin Users 3]: ../assets/screenshots/admin/admin-users-3.png
[Admin Users 4]: ../assets/screenshots/admin/admin-users-4.png
[Admin Users 5]: ../assets/screenshots/admin/admin-users-5.png
