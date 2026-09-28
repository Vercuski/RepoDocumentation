# <a id="ONIONARCH_Persistence_SqlServer_DependencyInjection"></a> Class DependencyInjection

Namespace: [ONIONARCH.Persistence.SqlServer](ONIONARCH.Persistence.SqlServer.md)  
Assembly: ONIONARCH.Persistence.SqlServer.dll  

Composition-root extension that opts a host in to the Microsoft SQL Server persistence provider.
This is the project's only public surface.

```csharp
public static class DependencyInjection
```

#### Inheritance

[object](https://learn.microsoft.com/dotnet/api/system.object) ← 
[DependencyInjection](ONIONARCH.Persistence.SqlServer.DependencyInjection.md)

#### Inherited Members

[object.Equals\(object?\)](https://learn.microsoft.com/dotnet/api/system.object.equals\#system\-object\-equals\(system\-object\)), 
[object.Equals\(object?, object?\)](https://learn.microsoft.com/dotnet/api/system.object.equals\#system\-object\-equals\(system\-object\-system\-object\)), 
[object.GetHashCode\(\)](https://learn.microsoft.com/dotnet/api/system.object.gethashcode), 
[object.GetType\(\)](https://learn.microsoft.com/dotnet/api/system.object.gettype), 
[object.MemberwiseClone\(\)](https://learn.microsoft.com/dotnet/api/system.object.memberwiseclone), 
[object.ReferenceEquals\(object?, object?\)](https://learn.microsoft.com/dotnet/api/system.object.referenceequals), 
[object.ToString\(\)](https://learn.microsoft.com/dotnet/api/system.object.tostring)

## Methods

### <a id="ONIONARCH_Persistence_SqlServer_DependencyInjection_AddSqlServer_ONIONARCH_Persistence_Providers_DatabaseProviderRegistry_"></a> AddSqlServer\(DatabaseProviderRegistry\)

Registers the Microsoft SQL Server provider. It is selected at startup when the <code>DatabasePlatform</code>
configuration's <code>QueryDbPlatform</code> or <code>CommandDbPlatform</code> is <code>MSSQL</code>
(case-insensitive).

```csharp
public static DatabaseProviderRegistry AddSqlServer(this DatabaseProviderRegistry registry)
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

A MSSQL provider is already registered.

