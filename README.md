# Futurum.Microsoft.Extensions.DependencyInjection.Core.Extensions

![license](https://img.shields.io/github/license/futurum-dev/dotnet.futurum.microsoft.extensions.dependencyinjection.core.extensions?style=for-the-badge)
![CI](https://img.shields.io/github/actions/workflow/status/futurum-dev/dotnet.futurum.microsoft.extensions.dependencyinjection.core.extensions/ci.yml?branch=main&style=for-the-badge)
[![Coverage Status](https://img.shields.io/coveralls/github/futurum-dev/dotnet.futurum.microsoft.extensions.dependencyinjection.core.extensions?style=for-the-badge)](https://coveralls.io/github/futurum-dev/dotnet.futurum.microsoft.extensions.dependencyinjection.core.extensions?branch=main)
[![NuGet version](https://img.shields.io/nuget/v/futurum.microsoft.extensions.dependencyinjection.core.extensions?style=for-the-badge)](https://www.nuget.org/packages/futurum.microsoft.extensions.dependencyinjection.core.extensions)

A dotnet library that extends [Futurum.Microsoft.Extensions.DependencyInjection](https://www.nuget.org/packages/Futurum.Microsoft.Extensions.DependencyInjection), making it fully compatible with [Futurum.Core](https://www.nuget.org/packages/Futurum.Core).

- [x] [Full compatibility](#buildserviceproviderwithstartables-extension-method) with [Futurum.Core](https://www.nuget.org/packages/Futurum.Core)

### BuildServiceProviderWithStartables extension method
If you are manually building the *IServiceProvider*, then you need to use *BuildServiceProviderWithStartablesAsync* extension method.
This will build the container as usual, but also starts all *IStartable* instances.

```csharp
var serviceProvider = await services.BuildServiceProviderWithStartablesAsync();
```

## TryGetService
Try to get the service object of the specified type.

```csharp
var result = serviceProvider.TryGetService<ITestService>();
```
