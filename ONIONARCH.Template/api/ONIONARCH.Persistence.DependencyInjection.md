# <a id="ONIONARCH_Persistence_DependencyInjection"></a> Class DependencyInjection

Namespace: [ONIONARCH.Persistence](ONIONARCH.Persistence.md)  
Assembly: ONIONARCH.Persistence.dll  

Composition-root extensions that register the Persistence layer: configuration options,
the database provider for each side of the CQRS split, and both the Dapper and EF Core
implementations of the Application-layer persistence ports.

```csharp
public static class DependencyInjection
```

#### Inheritance

[object](https://learn.microsoft.com/dotnet/api/system.object) ← 
[DependencyInjection](ONIONARCH.Persistence.DependencyInjection.md)

#### Inherited Members

[object.Equals\(object?\)](https://learn.microsoft.com/dotnet/api/system.object.equals\#system\-object\-equals\(system\-object\)), 
[object.Equals\(object?, object?\)](https://learn.microsoft.com/dotnet/api/system.object.equals\#system\-object\-equals\(system\-object\-system\-object\)), 
[object.GetHashCode\(\)](https://learn.microsoft.com/dotnet/api/system.object.gethashcode), 
[object.GetType\(\)](https://learn.microsoft.com/dotnet/api/system.object.gettype), 
[object.MemberwiseClone\(\)](https://learn.microsoft.com/dotnet/api/system.object.memberwiseclone), 
[object.ReferenceEquals\(object?, object?\)](https://learn.microsoft.com/dotnet/api/system.object.referenceequals), 
[object.ToString\(\)](https://learn.microsoft.com/dotnet/api/system.object.tostring)

## Methods

### <a id="ONIONARCH_Persistence_DependencyInjection_AddPersistenceRegistrations_Microsoft_Extensions_Hosting_IHostApplicationBuilder_"></a> AddPersistenceRegistrations\(IHostApplicationBuilder\)

Registers all Persistence-layer services.

```csharp
public static IHostApplicationBuilder AddPersistenceRegistrations(this IHostApplicationBuilder builder)
```

#### Parameters

`builder` [IHostApplicationBuilder](https://learn.microsoft.com/dotnet/api/microsoft.extensions.hosting.ihostapplicationbuilder)

The host builder to register services with.

#### Returns

 [IHostApplicationBuilder](https://learn.microsoft.com/dotnet/api/microsoft.extensions.hosting.ihostapplicationbuilder)

The same <code class="paramref">builder</code>, for chaining.

#### Exceptions

 [InvalidOperationException](https://learn.microsoft.com/dotnet/api/system.invalidoperationexception)

The <code>DatabasePlatform</code> configuration section is missing or invalid.

 [NotSupportedException](https://learn.microsoft.com/dotnet/api/system.notsupportedexception)

A configured database platform is not recognized.

