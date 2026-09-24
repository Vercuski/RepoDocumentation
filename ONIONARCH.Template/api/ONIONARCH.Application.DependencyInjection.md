# <a id="ONIONARCH_Application_DependencyInjection"></a> Class DependencyInjection

Namespace: [ONIONARCH.Application](ONIONARCH.Application.md)  
Assembly: ONIONARCH.Application.dll  

Composition-root extensions that register the Application layer's services.

```csharp
public static class DependencyInjection
```

#### Inheritance

[object](https://learn.microsoft.com/dotnet/api/system.object) ← 
[DependencyInjection](ONIONARCH.Application.DependencyInjection.md)

#### Inherited Members

[object.Equals\(object?\)](https://learn.microsoft.com/dotnet/api/system.object.equals\#system\-object\-equals\(system\-object\)), 
[object.Equals\(object?, object?\)](https://learn.microsoft.com/dotnet/api/system.object.equals\#system\-object\-equals\(system\-object\-system\-object\)), 
[object.GetHashCode\(\)](https://learn.microsoft.com/dotnet/api/system.object.gethashcode), 
[object.GetType\(\)](https://learn.microsoft.com/dotnet/api/system.object.gettype), 
[object.MemberwiseClone\(\)](https://learn.microsoft.com/dotnet/api/system.object.memberwiseclone), 
[object.ReferenceEquals\(object?, object?\)](https://learn.microsoft.com/dotnet/api/system.object.referenceequals), 
[object.ToString\(\)](https://learn.microsoft.com/dotnet/api/system.object.tostring)

## Methods

### <a id="ONIONARCH_Application_DependencyInjection_AddApplicationRegistration_Microsoft_Extensions_Hosting_IHostApplicationBuilder_"></a> AddApplicationRegistration\(IHostApplicationBuilder\)

Registers the Application layer: the [ISender](ONIONARCH.Application.Abstractions.ISender.md) dispatcher, every request handler
in this assembly, and the pipeline behaviors.

```csharp
public static IHostApplicationBuilder AddApplicationRegistration(this IHostApplicationBuilder builder)
```

#### Parameters

`builder` [IHostApplicationBuilder](https://learn.microsoft.com/dotnet/api/microsoft.extensions.hosting.ihostapplicationbuilder)

The host builder to register services with.

#### Returns

 [IHostApplicationBuilder](https://learn.microsoft.com/dotnet/api/microsoft.extensions.hosting.ihostapplicationbuilder)

The same <code class="paramref">builder</code>, for chaining.

