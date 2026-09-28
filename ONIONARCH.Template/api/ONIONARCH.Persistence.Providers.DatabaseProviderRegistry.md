# <a id="ONIONARCH_Persistence_Providers_DatabaseProviderRegistry"></a> Class DatabaseProviderRegistry

Namespace: [ONIONARCH.Persistence.Providers](ONIONARCH.Persistence.Providers.md)  
Assembly: ONIONARCH.Persistence.dll  

Composition-root registry of the database providers a host has opted into. Each provider project
contributes an extension method (<code>AddSqlServer</code>, <code>AddPostgreSql</code>, <code>AddMySql</code>) that
adds its provider here, so the core Persistence project resolves providers by configured platform
key without a compile-time dependency on any of them.

```csharp
public sealed class DatabaseProviderRegistry
```

#### Inheritance

[object](https://learn.microsoft.com/dotnet/api/system.object) ← 
[DatabaseProviderRegistry](ONIONARCH.Persistence.Providers.DatabaseProviderRegistry.md)

#### Inherited Members

[object.Equals\(object?\)](https://learn.microsoft.com/dotnet/api/system.object.equals\#system\-object\-equals\(system\-object\)), 
[object.Equals\(object?, object?\)](https://learn.microsoft.com/dotnet/api/system.object.equals\#system\-object\-equals\(system\-object\-system\-object\)), 
[object.GetHashCode\(\)](https://learn.microsoft.com/dotnet/api/system.object.gethashcode), 
[object.GetType\(\)](https://learn.microsoft.com/dotnet/api/system.object.gettype), 
[object.ReferenceEquals\(object?, object?\)](https://learn.microsoft.com/dotnet/api/system.object.referenceequals), 
[object.ToString\(\)](https://learn.microsoft.com/dotnet/api/system.object.tostring)

## Properties

### <a id="ONIONARCH_Persistence_Providers_DatabaseProviderRegistry_Platforms"></a> Platforms

The platform keys of every registered provider.

```csharp
public IReadOnlyCollection<string> Platforms { get; }
```

#### Property Value

 [IReadOnlyCollection](https://learn.microsoft.com/dotnet/api/system.collections.generic.ireadonlycollection\-1)<[string](https://learn.microsoft.com/dotnet/api/system.string)\>

## Methods

### <a id="ONIONARCH_Persistence_Providers_DatabaseProviderRegistry_Add_ONIONARCH_Persistence_Providers_IDatabaseProvider_"></a> Add\(IDatabaseProvider\)

Registers <code class="paramref">provider</code> under its [IDatabaseProvider.Platform](ONIONARCH.Persistence.Providers.IDatabaseProvider.md#ONIONARCH_Persistence_Providers_IDatabaseProvider_Platform) key.

```csharp
public DatabaseProviderRegistry Add(IDatabaseProvider provider)
```

#### Parameters

`provider` [IDatabaseProvider](ONIONARCH.Persistence.Providers.IDatabaseProvider.md)

The provider to register.

#### Returns

 [DatabaseProviderRegistry](ONIONARCH.Persistence.Providers.DatabaseProviderRegistry.md)

This registry, for chaining.

#### Exceptions

 [ArgumentNullException](https://learn.microsoft.com/dotnet/api/system.argumentnullexception)

<code class="paramref">provider</code> is <a href="https://learn.microsoft.com/dotnet/csharp/language-reference/keywords/null">null</a>.

 [InvalidOperationException](https://learn.microsoft.com/dotnet/api/system.invalidoperationexception)

A provider is already registered for the same platform key (compared case-insensitively).

### <a id="ONIONARCH_Persistence_Providers_DatabaseProviderRegistry_GetProvider_System_String_"></a> GetProvider\(string\)

Returns the provider registered for <code class="paramref">platform</code>.

```csharp
public IDatabaseProvider GetProvider(string platform)
```

#### Parameters

`platform` [string](https://learn.microsoft.com/dotnet/api/system.string)

The platform key from configuration; case-insensitive.

#### Returns

 [IDatabaseProvider](ONIONARCH.Persistence.Providers.IDatabaseProvider.md)

The registered provider.

#### Exceptions

 [ArgumentException](https://learn.microsoft.com/dotnet/api/system.argumentexception)

<code class="paramref">platform</code> is <a href="https://learn.microsoft.com/dotnet/csharp/language-reference/keywords/null">null</a>, empty, or whitespace.

 [NotSupportedException](https://learn.microsoft.com/dotnet/api/system.notsupportedexception)

No provider is registered for <code class="paramref">platform</code>. The message lists the registered platforms.

