---
template: overrides/main.html
title: Data Model &amp; Schema
---

# Data Model &amp; Schema

Cellmobs offers a highly flexible core data model, consisting of commonly used entities such as Identities (Users), Organizations, Products, Content (Files), and more. This flexibility allows users to build a wide range of applications tailored to their specific requirements. The core data model can be extended in two ways: Custom Field Templates and custom Models.

## Custom Field Templates

Custom Field Templates provide a convenient way to extend existing model classes with additional fields. Users can define sets of fields as templates that can be attached to new or modified entities. This allows users to add custom attributes to entities, enabling them to capture and store additional information specific to their application's requirements. Custom Field Templates make it easy to expand the core data model without the need for complex code modifications or database schema changes.

Click here to learn how to [configure customer field templates](/app-console/manage-templates/#custom-fields).

<figure markdown>
![Custom Fields](../assets/app-console/custom-fields-editor.png){loading=lazy}
    <figcaption>Custom Field Templates</figcaption>
</figure>


## Entity Requirements

In addition to extending the core data model, Cellmobs supports Entity Requirements, a feature designed to validate entity field values based on configurable business rules in support of certain use cases and [workflows](/setup/setting-up-workflow). 

Entity Requirements help ensure data consistency and integrity by enforcing specific conditions and constraints on entity attributes. This allows users to maintain high-quality data in their applications, ultimately improving the overall user experience and reliability of the system.

<figure markdown>
![Entity Requirements](../assets/setup/requirements-sample.png){loading=lazy}
    <figcaption>Entity Requirements Example</figcaption>
</figure>

Click here to learn how to [configure entity requirements](/app-console/manage-workflow).


## Custom Models

For more advanced use cases, Cellmobs allows users to create entirely custom Models. This feature provides even greater flexibility, enabling users to define their own entity types with custom attributes, relationships, and behavior. Custom Models can be used alongside the core data model to build sophisticated applications that cater to unique business requirements. 

Custom Models are still in the experimental stage and will be rolled out later this year. 

<br><br>