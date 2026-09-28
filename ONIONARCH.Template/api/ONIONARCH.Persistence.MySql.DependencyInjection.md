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

## Methods

### <a id="ONIONARCH_Persistence_MySql_DependencyInjection_AddMySql_ONIONARCH_Persistence_Providers_DatabaseProviderRegistry_"></a> AddMySql\(DatabaseProviderRegistry\)

Registers the MySQL provider. It is selected at startup when the <code>DatabasePlatform</code>
configuration's <code>QueryDbPlatform</code> or <code>CommandDbPlatform</code> is <code>MySQL</code>
(case-insensitive).

```csharp
public static DatabaseProviderRegistry AddMySql(this DatabaseProviderRegistry registry)
```

#### Parameters

`registry` DatabaseProviderRegistry

The registry passed to <code>AddPersistenceRegistrations</code>.

#### Returns

 DatabaseProviderRegistry

The same <code class="paramref">registry</code>, for chaining.

#### Exceptions

 [ArgumentNullException](https://learn.microsoft.com/dotnet/api/system.argumentnullexception)

<code class="paramref">registry</code> is <a href="https://learn.microsoft.com/dotnet/csharp/language-reference/keywords/null">null</a>.

 [InvalidOperationException](https://learn.microsoft.com/dotnet/api/system.invalidoperationexception)

A MySQL provider is already registered.

