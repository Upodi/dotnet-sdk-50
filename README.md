# Upodi SDK 5.0 for Microsoft .NET Core Framework [![NuGet](https://img.shields.io/nuget/v/Upodi.SDK.5.svg)](https://www.nuget.org/packages/Upodi.SDK.5/)
Upodi SDK for .NET developers enables easy to use integration and programming .NET applications.

Support .NET Standard 2.1, .NET Core 5/6/7 and .NET Framework 4.8. [Download from here](https://www.nuget.org/packages/Upodi.SDK.5/) or using your favorite NuGet package manager.

## Overview
* [NuGet package](https://www.nuget.org/packages/Upodi.Sdk/)
* [Documentation](https://docs.upodi.com)
* [API Documentation](https://docs.upodi.com/v5.0/reference)
* [License](https://github.com/Upodi/dotnet-sdk/blob/master/LICENSE)
* [Request a trial](https://www.upodi.com/register/walkthrough/)
* [Stack Overflow](https://stackoverflow.com/questions/tagged/upodi)

## Getting started
Retrieve your secret key from the [Upodi Portal](https://portal.upodi.io).

### Installations
Using the .NET Core command-line interface (CLI) tools:

```cmd
dotnet add package Upodi.SDK.5
```

Using the NuGet Command Line Interface (CLI):

```cmd
nuget install Upodi.SDK.5
```

Using the Package Manager Console:

```cmd
Install-Package Upodi.SDK.5
```

From within Visual Studio:

1. Open the Solution Explorer.
2. Right-click on a project within your solution.
3. Click on Manage NuGet Packages...
4. Click on the Browse tab and search for "Upodi.SDK.5".
5. Click on the Upodi.SDK package, select the appropriate version in the right-tab and click Install.

### Initialization
```csharp
UpodiClient upodi = new UpodiClient(
                new Credentials({secret api key}));

var listOfCustomer = await upodi.Customers.ListAsync();
```
## Documentation
For a comprehensive list of examples, check out the [API Documentation](https://docs.upodi.com/v5.0/reference).

### Non-Mutable Fields
Upodi SDK provides properties of entities subject to the Upodi API as documented here [https://docs.upodi.com/v5.0/reference](https://docs.upodi.com/v5.0/reference). However a few changes apply as some properties are controlled by the API - and the Upodi SDK only provides a pass through.

* **ID**. *Guid*. The ID is required to create objects via the Upodi API. However the ID will be changes upon creation as the ID is controlled by Upodi. Example: As such, you will have to create a new customer with ID = Guid.NewGuid(), which then is returned after creation with a system assigned ID.
* **CreatedDate** and **ModifiedDate**. *DateTime*. These fields are always set by Upodi.
* **CreatedBy** and **ModifiedBy**. *Guid*. These fields are always set by Upodi.

The full list of non-mutable fields can be found here [https://docs.upodi.com/v5.0/reference](https://docs.upodi.com/v5.0/reference).

## Support
New features and bug fixes are released on the latest major version of the Upodi SDK. If you are on an older major version, we recommend that you upgrade to the latest in order to use the new features and bug fixes including those for security vulnerabilities. Older major versions of the package will continue to be available for use, but will not be receiving any updates.
