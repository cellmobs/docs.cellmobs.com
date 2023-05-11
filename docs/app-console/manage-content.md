---
template: overrides/main.html
title: Content
---

# Content

Content is a central entity in the Cellmobs platform, representing all file-based data, such as images, documents, and videos. It plays a crucial role in many aspects of the platform and can be associated with various [Cellmobs entities](/setup/model-schema), including [Products](/app-console/manage-products), DealsTerms, Feeds, Channels, and more.

Developers have the flexibility to use Cellmobs to host their static content or connect their Cellmobs App to their own AWS S3 account or other cloud storage locations such as Dropbox, Box, Google Drive, or OneDrive. This versatility allows developers to choose the storage solution that best fits their requirements and preferences.

Content in Cellmobs is always associated with a primary [Organization](/app-console/manage-organizations). This association determines which users have access to read and modify the content, ensuring that content management is securely controlled within the platform.

## Content Types

Cellmobs supports different Content Types. They are typically derived from the file mimetype during uploads unless they are explictly provided. It is goog practive to pass the ContentType parameter along with a configured FileType. 

The main content types are:

| Content Type | Description | 
| ---------|----------|
| `IMAGE` | All public Images Mime Types | 
| `VIDEO` | All public Video files e.g. mp4, mov, mpeg | 
| `AUDIO` | All public Audio files | 
| `DOCUMENT` | All public documents e.g. doc, pdf, ppt, etc | 
| `FOLDER` | Represents the path to a folder. Either on S3 or another supported storage API  | 
| `SECURE_FILE` | Files that are uploaded to private AWS bucket that is only accessible to authorized usersl where file access is proxied through Cellmobs ACL | 

FileType is a Content sub type and defines the business use case of a given file. Some file types are [system types](/setup/image-settings/?h=filetype#system-file-types) while others can be freely defined by the application developer. 

Images settings for `IMAGE` file types for example are configured using [Image Settings](/setup/image-settings).   

## Renditions

In Cellmobs, when an image file is uploaded, the system by default generates multiple renditions of that image base on configured [Image Settings](/setup/image-settings). Rendition profiles for other Content Types will be supported soon 

For images renditions are different versions of the original image but in various sizes and dimensions. This automatic generation of image renditions allows your application to serve the most appropriate version of an image based on the context, such as the device screen size or network conditions, improving both performance and user experience.

These renditions could be thumbnails for list views, medium-sized images for detail views, and large or full-sized images for close-up views or zooming. This approach ensures that you always have the right size image for any situation, and you don't have to manually create these versions yourself, saving considerable time and effort.

However, there may be cases where you do not want Cellmobs to generate these renditions. For example, you may want to have full control over how images are resized or manipulated, or you may want to minimize storage usage. In these cases, you can pass the `render=false` parameter during the image upload process. When this parameter is used, Cellmobs will not generate any renditions of the uploaded image, and only the original image will be stored and available for use in your application.

Remember, the decision to generate renditions or not will depend on your specific needs and the requirements of your application. While the automatic generation of renditions can improve performance and user experience, it may not be necessary or desirable in all cases.

## Creating Content

Use Cellmobs to create unique web and mobile content - from articles, and infographics to videos, GIFs and memes, which can be used while creating products.


- Go to [Content Section](https://console.cellmobs.com/admin/content/list)
- Click on Add Content 
- Enter the name of the “Content”  
- Provide the “Organization” name 
- Select the content type (Image, Video, Audio, Folder, Caption, Document) 
- Select the File Type from the drop down (Custom Image, Identity AVATAR, Identity Header, Organization Logo, Product Image, Secure File, Tag header, Tag Image) 
- Provide the description of the content that you want to publish along with the content (Image/Video etc.)

<figure markdown>
![Admin Content 1][Admin Content 1]
</figure>

- Click on Choose file and upload the content  
- Click on Save/Upload and it creates the content, it takes you to the Edit content page 
- Go to the Renditions section and see how the images look like with 6 different sizes (ex: large, small etc.,) 
- If you want to change the image, click on Upload content and select another image and it gets changed. 

<figure markdown>
![Admin Content 2][Admin Content 2]
</figure>

- Click on Save Changes 

<figure markdown>
![Admin Content 3][Admin Content 3]
</figure>


[Admin Content 1]: ../assets/screenshots/admin/admin-content-1.png
[Admin Content 2]: ../assets/screenshots/admin/admin-content-2.png
[Admin Content 3]: ../assets/screenshots/admin/admin-content-3.png

*

## Sync Content across Apps 

Cellmobs can sync files and their associated metadata across apps. This comes in handy when sharing assets, like product images or documents, among various apps in your portfolio.

[SHOW MODAL EXAMPLE]


<br><br>
