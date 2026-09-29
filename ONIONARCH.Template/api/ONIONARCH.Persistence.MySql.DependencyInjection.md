# <a id="ONIONARCH_Persistence_MySql_DependencyInjection"></a> Class DependencyInjection

Namespace: [ONIONARCH.Persistence.MySql](ONIONARCH.Persistence.MySql.md)  
Assembly: ONIONARCH.Persistence.MySql.dll  

Composition-root extension that opts a host in to the MySQL persistence provider.
This is the project's only public surface.

```csharp
public static class DependencyInjection
```

#### Inheritance

[object](https://learn.microsoft.com/dotnet/api/system.object) ← 
[DependencyInjection](ONIONARCH.Persistence.MySql.DependencyInjection.md)

#### Inherited Members

[object.Equals\(object?\)](https://learn.microsoft.com/dotnet/api/system.object.equals\#system\-object\-equals\(system\-object\)), 
[object.Equals\(object?, object?\)](https://learn.microsoft.com/dotnet/api/system.object.equals\#system\-object\-equals\(system\-object\-system\-object\)), 
[object.GetHashCode\(\)](https://learn.microsoft.com/dotnet/api/system.object.gethashcode), 
[object.GetType\(\)](https://learn.microsoft.com/dotnet/api/system.object.gettype), 
[object.MemberwiseClone\(\)](https://learn.microsoft.com/dotnet/api/system.object.memberwiseclone), 
[object.ReferenceEquals\(object?, object?\)](https://learn.microsoft.com/dotnet/api/system.object.referenceequals), 
[object.ToString\(\)](https://learn.microsoft.com/dotnet/api/system.object.tostring)

## Fields

### <a id="ONIONARCH_Persistence_MySql_DependencyInjection_ServerVersionConfigurationKey"></a> ServerVersionConfigurationKey

The configuration key holding the MySQL/MariaDB server version EF Core targets, e.g.
<code>8.4.0-mysql</code> or <code>11.4.2-mariadb</code>.

```csharp
public const string ServerVersionConfigurationKey = "DatabasePlatform:MySqlServerVersion"
```

#### Field Value

 [string](https://learn.microsoft.com/dotnet/api/system.string)

## Methods

### <a id="ONIONARCH_Persistence_MySql_DependencyInjection_AddMySql_ONIONARCH_Persistence_Providers_DatabaseProviderRegistry_Microsoft_Extensions_Configuration_IConfiguration_"></a> AddMySql\(DatabaseProviderRegistry, IConfiguration\)

Registers the MySQL provider. It is selected at startup when the <code>DatabasePlatform</code>
configuration's <code>QueryDbPlatform</code> or <code>CommandDbPlatform</code> is <code>MySQL</code>
(case-insensitive).

```csharp
public static DatabaseProviderRegistry AddMySql(this DatabaseProviderRegistry registry, IConfiguration configuration)
```

#### Parameters

`registry` DatabaseProviderRegistry

The registry passed to <code>AddPersistenceRegistrations</code>.

`configuration` [IConfiguration](https://learn.microsoft.com/dotnet/api/microsoft.extensions.configuration.iconfiguration)

The host configuration to read the server version from.

#### Returns

 DatabaseProviderRegistry

The same <code class="paramref">registry</code>, for chaining.

#### Remarks

The server version is read from [DependencyInjection.ServerVersionConfigurationKey](ONIONARCH.Persistence.MySql.DependencyInjection.md#ONIONARCH_Persistence_MySql_DependencyInjection_ServerVersionConfigurationKey) and validated here,
so a missing or malformed value fails at startup rather than on the first database call. It is
required whenever the provider is registered, even if neither side is currently configured for
MySQL; remove the registration to drop the requirement. One version applies to both CQRS sides.

#### Exceptions

 [ArgumentNullException](https://learn.microsoft.com/dotnet/api/system.argumentnullexception)

<code class="paramref">registry</code> or <code class="paramref">configuration</code> is <a href="https://learn.microsoft.com/dotnet/csharp/language-reference/keywords/null">null</a>.

 [InvalidOperationException](https://learn.microsoft.com/dotnet/api/system.invalidoperationexception)

The server version is missing or cannot be parsed, or a MySQL provider is already registered.

