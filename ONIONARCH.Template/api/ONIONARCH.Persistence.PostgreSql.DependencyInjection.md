# <a id="ONIONARCH_Persistence_PostgreSql_DependencyInjection"></a> Class DependencyInjection

Namespace: [ONIONARCH.Persistence.PostgreSql](ONIONARCH.Persistence.PostgreSql.md)  
Assembly: ONIONARCH.Persistence.PostgreSql.dll  

Composition-root extension that opts a host in to the PostgreSQL persistence provider.
This is the project's only public surface.

```csharp
public static class DependencyInjection
```

#### Inheritance

[object](https://learn.microsoft.com/dotnet/api/system.object) ← 
[DependencyInjection](ONIONARCH.Persistence.PostgreSql.DependencyInjection.md)

#### Inherited Members

[object.Equals\(object?\)](https://learn.microsoft.com/dotnet/api/system.object.equals\#system\-object\-equals\(system\-object\)), 
[object.Equals\(object?, object?\)](https://learn.microsoft.com/dotnet/api/system.object.equals\#system\-object\-equals\(system\-object\-system\-object\)), 
[object.GetHashCode\(\)](https://learn.microsoft.com/dotnet/api/system.object.gethashcode), 
[object.GetType\(\)](https://learn.microsoft.com/dotnet/api/system.object.gettype), 
[object.MemberwiseClone\(\)](https://learn.microsoft.com/dotnet/api/system.object.memberwiseclone), 
[object.ReferenceEquals\(object?, object?\)](https://learn.microsoft.com/dotnet/api/system.object.referenceequals), 
[object.ToString\(\)](https://learn.microsoft.com/dotnet/api/system.object.tostring)

## Methods

### <a id="ONIONARCH_Persistence_PostgreSql_DependencyInjection_AddPostgreSql_ONIONARCH_Persistence_Providers_DatabaseProviderRegistry_"></a> AddPostgreSql\(DatabaseProviderRegistry\)

Registers the PostgreSQL provider. It is selected at startup when the <code>DatabasePlatform</code>
configuration's <code>QueryDbPlatform</code> or <code>CommandDbPlatform</code> is <code>PostgreSQL</code>
(case-insensitive).

```csharp
public static DatabaseProviderRegistry AddPostgreSql(this DatabaseProviderRegistry registry)
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

A PostgreSQL provider is already registered.

