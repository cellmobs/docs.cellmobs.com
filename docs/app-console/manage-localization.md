---
template: overrides/main.html
title: Localization
---

# Localization

Cellmobs's App Console is designed with localization and flexible taxonomy in mind, allowing developers to adapt their applications to various use cases, business verticals, and language requirements.

The console is built around tokenized entities, form field labels, and text, meaning that each piece of text is associated with a unique token (aka code). This provides a highly adaptable environment where you can replace the default terminology with terminology that fits your specific application's needs. For example, in a healthcare application, "Users" might be replaced with "Patients," or in an educational context, "Organizations" might be replaced with "Schools" or "Classes."

Moreover, these tokens support localization, allowing you to translate your application into different languages. You can specify the translations for each token, and the console will display the appropriate language based on the user's settings or your predefined configuration. This localization capability opens up your application to a global audience and ensures a user-friendly experience for users of different language backgrounds.


## Configure Localization 

Cellmobs makes it simple to customize and localize your application. Each term or phrase in the console UI or client application is represented by a token, or `code`. This code corresponds to a value that is the actual string displayed in the user interface. For example, the code `user.email` might correspond to the value 'Email Address'. 

If you want to customize the terminology in your application, you simply replace the default value associated with each code. This is done by clicking on the value in the "Message" column in the console and entering your desired string. This flexibility allows you to align the language used in your application with your specific use case or industry terminology.

Moreover, if you need additional terms that are not covered by the default codes, you can add new code-message pairs. This allows you to extend the vocabulary used in your application beyond the default set provided by Cellmobs.

For localization, if you have the [translation API]() enabled, any new or updated message values will be automatically translated into the languages you have chosen to support. This means that if you update the 'Email Address' value to 'Correo Electrónico' in Spanish, for instance, this new value will be used for Spanish-speaking users of your application.

<figure markdown>
![Taxonomy &amp; Localization](../assets/app-console/localization-editor.png){loading=lazy}
    <figcaption>Taxonomy &amp; Localization</figcaption>
</figure>


<br><br>