# Upodi SDK 5.0 for Microsoft .NET Core Framework [![NuGet](https://img.shields.io/nuget/v/Upodi.SDK.5.svg)](https://www.nuget.org/packages/Upodi.SDK.5/)
Upodi SDK Core for C# and .net developers enables easy to use integration and programming core applications.

Upodi SDK for .NET Core 2.1 provided by NuGet. [Download from here](https://www.nuget.org/packages/Upodi.SDK.5/) or using your favorite NuGet package manager.

## Overview
* [NuGet package](https://www.nuget.org/packages/Upodi.Sdk/)
* [Documentation](https://docs.upodi.com)
* [API Documentation](https://docs.upodi.com/v2.0/reference)
* [License](https://github.com/Upodi/dotnet-sdk/blob/master/LICENSE)
* [Request a trial](https://www.upodi.com/register/walkthrough/)
* [Stack Overflow](https://stackoverflow.com/questions/tagged/upodi)

## Getting started

### Initialization
```
UpodiClient upodi = new UpodiClient(
                new Credentials({secret api key}));
var listOfCustomer = upodi.Customers.List();
```

### Non-Mutable Fields
Upodi SDK provides properties of entities subject to the Upodi API as documented here [https://docs.upodi.com/v2.0/reference](https://docs.upodi.com/v2.0/reference). However a few changes apply as some properties are controlled by the API - and the Upodi SDK only provides a pass through.

* **ID**. *Guid*. The ID is required to create objects via the Upodi API. However the ID will be changes upon creation as the ID is controlled by Upodi. Example: As such, you will have to create a new customer with ID = Guid.NewGuid(), which then is returned after creation with a system assigned ID.
* **CreatedDate** and **ModifiedDate**. *DateTime*. These fields are always set by Upodi.
* **CreatedBy** and **ModifiedBy**. *Guid*. These fields are always set by Upodi.

The full list of non-mutable fields can be found here [https://docs.upodi.com/v2.0/reference](https://docs.upodi.com/v2.0/reference).

## Preview edition
Latest and experimental features are subject to the preview version. [![NuGet](https://img.shields.io/nuget/v/Upodi.SDK.Preview.svg)](https://www.nuget.org/packages/Upodi.SDK.Preview/)
