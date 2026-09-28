# <a id="ONIONARCH_Persistence_DependencyInjection"></a> Class DependencyInjection

Namespace: [ONIONARCH.Persistence](ONIONARCH.Persistence.md)  
Assembly: ONIONARCH.Persistence.dll  

Composition-root extensions that register the Persistence layer: configuration options,
the database provider for each side of the CQRS split (resolved from the providers the host
registers in a [DatabaseProviderRegistry](ONIONARCH.Persistence.Providers.DatabaseProviderRegistry.md)), and both the Dapper and EF Core
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

### <a id="ONIONARCH_Persistence_DependencyInjection_AddPersistenceRegistrations_Microsoft_Extensions_Hosting_IHostApplicationBuilder_System_Action_ONIONARCH_Persistence_Providers_DatabaseProviderRegistry__"></a> AddPersistenceRegistrations\(IHostApplicationBuilder, Action<DatabaseProviderRegistry\>\)

Registers all Persistence-layer services.

```csharp
public static IHostApplicationBuilder AddPersistenceRegistrations(this IHostApplicationBuilder builder, Action<DatabaseProviderRegistry> configureProviders)
```

#### Parameters

`builder` [IHostApplicationBuilder](https://learn.microsoft.com/dotnet/api/microsoft.extensions.hosting.ihostapplicationbuilder)

The host builder to register services with.

`configureProviders` [Action](https://learn.microsoft.com/dotnet/api/system.action\-1)<[DatabaseProviderRegistry](ONIONARCH.Persistence.Providers.DatabaseProviderRegistry.md)\>

Opts the host in to the provider-specific projects it references, e.g.
<code>providers.AddSqlServer()</code>. The query and command sides may use different platforms, so
register every platform either side's configuration can name.

#### Returns

 [IHostApplicationBuilder](https://learn.microsoft.com/dotnet/api/microsoft.extensions.hosting.ihostapplicationbuilder)

The same <code class="paramref">builder</code>, for chaining.

#### Exceptions

 [ArgumentNullException](https://learn.microsoft.com/dotnet/api/system.argumentnullexception)

<code class="paramref">configureProviders</code> is <a href="https://learn.microsoft.com/dotnet/csharp/language-reference/keywords/null">null</a>.

 [InvalidOperationException](https://learn.microsoft.com/dotnet/api/system.invalidoperationexception)

The <code>DatabasePlatform</code> configuration section is missing or invalid.

 [NotSupportedException](https://learn.microsoft.com/dotnet/api/system.notsupportedexception)

A configured database platform has no registered provider.

