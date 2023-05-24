---
template: overrides/main.html
title: Plugins
---

# Plugins

[Open Services Gateway initiative](https://www.osgi.org/) (OSGi) is a well-established framework that allows for module-based development, providing a high level of flexibility and adaptability for Java applications. By adopting OSGi, Cellmobs enhances its extensibility, providing a more robust and adaptable platform for developers. Here's how:

### Dynamic Module System
OSGi's dynamic module system allows developers to add, update, or remove modules at runtime without restarting the entire application. This not only saves time during the development process, but also enables a high degree of customization as developers can add new functionalities to Cellmobs applications on-the-fly.


### Service-Oriented Architecture
OSGi promotes a service-oriented architecture, where each module, also known as a bundle, provides services to other modules and consumes services provided by others. This encourages loose coupling, which leads to a more modular and maintainable application. In the context of Cellmobs, developers can easily integrate various services into their application by merely installing the corresponding OSGi bundles.


### Efficient Resource Management
With OSGi, each bundle operates in its own namespace, which helps in efficient resource management and eliminates conflicts between different bundles. This makes Cellmobs more reliable and stable, especially when running multiple plugins or integrations.


### Rich Ecosystem of Bundles
OSGi boasts a rich ecosystem of ready-to-use bundles, extending the capabilities of the Cellmobs platform. Developers can leverage these bundles to add specific functionalities to their application, reducing development time and increasing efficiency.

### Versioning and Compatibility
OSGi handles versioning and compatibility effectively. Different versions of a bundle can coexist, and each bundle can specify the versions of services it requires. This makes it easier for Cellmobs applications to manage dependencies and avoid conflicts.


Cellmobs' use of OSGi brings a new level of adaptability, modularity, and extensibility to the platform. It simplifies the integration of third-party services and the development of custom plugins, offering a versatile solution to meet diverse business needs.

## Example

Here's an example of how to create an OSGi interface, implementation, and activator for a plug-in that will save a new contact to the Mailchimp REST API:

**OSGi interface:**

```java
public interface MailchimpService {
    void addContact(String email, String firstName, String lastName) throws Exception;
}
```

**OSGi implementation:**

```java
import com.mashape.unirest.http.HttpResponse;
import com.mashape.unirest.http.Unirest;
import org.osgi.service.component.annotations.Component;

@Component
public class MailchimpServiceImpl implements MailchimpService {

    private static final String API_KEY = "YOUR_API_KEY_HERE";
    private static final String API_ENDPOINT = "https://us1.api.mailchimp.com/3.0/lists/YOUR_LIST_ID/members";

    @Override
    public void addContact(String email, String firstName, String lastName) throws Exception {

        String jsonPayload = "{\"email_address\":\"" + email + "\",\"status\":\"subscribed\",\"merge_fields\":{\"FNAME\":\"" + firstName + "\",\"LNAME\":\"" + lastName + "\"}}";

        HttpResponse<String> response = Unirest.post(API_ENDPOINT)
                .header("Authorization", "Basic " + API_KEY)
                .header("Content-Type", "application/json")
                .body(jsonPayload)
                .asString();

        if (response.getStatus() != 200) {
            throw new Exception("Failed to add contact to Mailchimp list: " + response.getBody());
        }
    }
}
```

Make sure to replace `YOUR_API_KEY_HERE` with your Mailchimp API key and `YOUR_LIST_ID` with the ID of the list to which you want to add the new contact.

**OSGi activator:**

```java
import org.osgi.framework.BundleActivator;
import org.osgi.framework.BundleContext;
import org.osgi.framework.ServiceRegistration;

public class Activator implements BundleActivator {

    private ServiceRegistration<MailchimpService> registration;

    @Override
    public void start(BundleContext bundleContext) throws Exception {
        registration = bundleContext.registerService(MailchimpService.class, new MailchimpServiceImpl(), null);
    }

    @Override
    public void stop(BundleContext bundleContext) throws Exception {
        registration.unregister();
    }
}
```

The activator is responsible for registering the `MailchimpService` implementation as an OSGi service. The `start` method is called when the bundle is started, and the `registerService` method is used to register the service. The `stop` method is called when the bundle is stopped, and the `unregister` method is used to unregister the service.

Note that you will need to include the `Unirest` and `org.json` libraries in your OSGi bundle. You can do this by adding the libraries to the bundle's classpath, or by using a dependency management tool like Maven or Gradle to automatically include the libraries in the bundle.


## Packaging an OSGI Bundle

The main components of an OSGi bundle are:

- **Java classes:** The Java classes that make up the functionality of the bundle. These classes are typically organized into packages and may include interfaces, implementation classes, and utility classes.

- **Manifest file:** The manifest file is a text file that provides metadata about the bundle, such as its name, version, package exports and imports, and required dependencies. The manifest file must be named `MANIFEST.MF` and located in the `META-INF` directory of the bundle.

- **Resources:** The bundle may include non-Java resources such as images, configuration files, and other assets. These resources must be placed in the appropriate directories within the bundle's file structure.

- **Libraries:** The bundle may depend on third-party libraries or other bundles. These dependencies must be packaged with the bundle, typically in a `lib` directory.

- **Bundle activatorz** An optional Java class that is used to initialize and start the bundle when it is activated by the OSGi framework. The activator class must implement the `BundleActivator` interface.

Before installation, an OSGi bundle is packaged as a JAR file with the following structure:

```
my-bundle/
├── META-INF/
│   └── MANIFEST.MF
├── com/
│   └── mycompany/
│       └── mybundle/
│           ├── MyClass1.class
│           ├── MyClass2.class
│           └── ...
├── lib/
│   └── some-library.jar
└── resources/
    ├── config.properties
    └── images/
        ├── image1.png
        └── image2.png
```

The `META-INF/MANIFEST.MF` file is required and must contain the bundle's metadata, as described above. The `com/mycompany/mybundle` directory contains the Java classes that make up the bundle's functionality. The `lib` directory contains any third-party libraries that the bundle depends on. The `resources` directory contains any non-Java resources, such as configuration files and images.

Once the JAR file is created, it can be installed into an OSGi framework by copying it to the framework's `bundle` directory. The OSGi framework will read the `MANIFEST.MF` file to determine the bundle's metadata and dependencies, and will then activate and start the bundle.

Here's an example `MANIFEST.MF` file for the Mailchimp plugin that I described earlier:

```
Manifest-Version: 1.0
Bundle-ManifestVersion: 2
Bundle-Name: Mailchimp Plugin
Bundle-SymbolicName: com.example.mailchimpplugin
Bundle-Version: 1.0.0
Bundle-Activator: com.example.mailchimpplugin.Activator
Bundle-Vendor: Example Company
Import-Package: org.osgi.framework;version="1.3.0",
 com.mashape.unirest.http;version="[1.4,2)",
 org.json;version="[20211205,2022)"
Export-Package: com.example.mailchimpplugin.api
```

This manifest file includes the following metadata:

- `Bundle-ManifestVersion` - The version of the bundle manifest specification.
- `Bundle-Name` - A human-readable name for the bundle.
- `Bundle-SymbolicName` - A unique identifier for the bundle.
- `Bundle-Version` - The version of the bundle.
- `Bundle-Activator` - The fully qualified class name of the bundle's activator.
- `Bundle-Vendor` - The name of the company or organization that created the bundle.
- `Import-Package` - The list of packages that the bundle depends on. In this case, the bundle depends on the `org.osgi.framework`, `com.mashape.unirest.http`, and `org.json` packages.
- `Export-Package` - The list of packages that the bundle exports. In this case, the bundle exports the `com.example.mailchimpplugin.api` package, which contains the `MailchimpService` interface.

Note that the version ranges specified for the imported packages (`[1.4,2)` and `[20211205,2022)`) indicate that the bundle requires a minimum version of `1.4` for the `com.mashape.unirest.http` package and a minimum version of `20211205` for the `org.json` package, but is compatible with any version up to (but not including) version `2.0` and `2022`, respectively.

## Dependency Resolution

In OSGi, bundles can depend on other bundles, and the OSGi framework provides a mechanism to manage these dependencies. When a bundle is installed into the framework, the framework examines the bundle's `MANIFEST.MF` file to determine its dependencies. 

OSGi resolves dependencies by comparing the requirements of a bundle with the capabilities of other bundles. A requirement is a declaration by a bundle of what it needs, while a capability is a declaration by a bundle of what it provides. 

A requirement can be of two types: `Import-Package` or `Require-Bundle`. `Import-Package` is used to declare a dependency on a specific package, while `Require-Bundle` is used to declare a dependency on another bundle.

A capability can be of two types: `Export-Package` or `Provide-Capability`. `Export-Package` is used to declare a package that the bundle provides, while `Provide-Capability` is used to declare a custom capability that the bundle provides.

When the OSGi framework installs a bundle, it examines the bundle's requirements and capabilities to determine which other bundles can satisfy the requirements. The framework maintains a dependency graph that tracks the dependencies between bundles. If a required capability is not present in the framework, the bundle cannot be resolved and will fail to start.

OSGi uses a dynamic linking mechanism, which means that dependencies are resolved at runtime, rather than at compile time. This allows bundles to be installed and uninstalled dynamically, without affecting the rest of the system.

When a bundle is started, its activator is called to perform any initialization tasks, such as registering services with the OSGi service registry. If the activator fails to start, the bundle will be stopped and its services will be unregistered.

In summary, OSGi bundles resolve dependencies by examining the requirements and capabilities of bundles, and dynamically linking them at runtime. This allows for a highly modular and flexible system, where bundles can be installed and uninstalled dynamically, without affecting the rest of the system.

<br><br>