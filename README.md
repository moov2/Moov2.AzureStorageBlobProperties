# Microsoft Azure Storage Blob Properties

Module for [Orchard CMS](http://orchardproject.net) giving the ability to define properties for files uploaded to Microsoft Azure Blob Storage Out of the box Orchard supplies modules that handle uploading files to blob storage on Azure, however there is currently no way to define [properties on the blob](https://msdn.microsoft.com/en-us/library/microsoft.windowsazure.storage.blob.blobproperties.aspx), e.g. cache control. This module supresses `AzureBlobStorageProvider` and handles setting properties on the blog when a file is being uploaded. Property values should be configured in the `appSettings` of the root `Web.config` for the Orchard site. 

## Properties

Below is a list of properties that can be configured. If there is a property you require then feel free open an issue or submit a pull request.

### Cache Control

Sets the cache control value for the blob, which gives [desirable performance improvements](https://developers.google.com/web/fundamentals/performance/optimizing-content-efficiency/http-caching#cache-control). Add `Orchard.Azure.Media.StorageCacheControl` to the `appSettings` in the `Web.config` for the Orchard site. An example value is `public, max-age=31536000`.

## Release

*This module is currently under development.*