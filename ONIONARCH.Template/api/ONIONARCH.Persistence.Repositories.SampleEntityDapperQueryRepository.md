# <a id="ONIONARCH_Persistence_Repositories_SampleEntityDapperQueryRepository"></a> Class SampleEntityDapperQueryRepository

Namespace: [ONIONARCH.Persistence.Repositories](ONIONARCH.Persistence.Repositories.md)  
Assembly: ONIONARCH.Persistence.dll  

Dapper implementation of [ISampleEntityDapperQueryRepository](ONIONARCH.Application.Abstractions.Repositories.ISampleEntityDapperQueryRepository.md), executing
parameterized SQL against the <code>SampleTable</code> table in the query database.

```csharp
public sealed class SampleEntityDapperQueryRepository : ISampleEntityDapperQueryRepository
```

#### Inheritance

[object](https://learn.microsoft.com/dotnet/api/system.object) ← 
[SampleEntityDapperQueryRepository](ONIONARCH.Persistence.Repositories.SampleEntityDapperQueryRepository.md)

#### Implements

ISampleEntityDapperQueryRepository

#### Inherited Members

[object.Equals\(object?\)](https://learn.microsoft.com/dotnet/api/system.object.equals\#system\-object\-equals\(system\-object\)), 
[object.Equals\(object?, object?\)](https://learn.microsoft.com/dotnet/api/system.object.equals\#system\-object\-equals\(system\-object\-system\-object\)), 
[object.GetHashCode\(\)](https://learn.microsoft.com/dotnet/api/system.object.gethashcode), 
[object.GetType\(\)](https://learn.microsoft.com/dotnet/api/system.object.gettype), 
[object.ReferenceEquals\(object?, object?\)](https://learn.microsoft.com/dotnet/api/system.object.referenceequals), 
[object.ToString\(\)](https://learn.microsoft.com/dotnet/api/system.object.tostring)

## Constructors

### <a id="ONIONARCH_Persistence_Repositories_SampleEntityDapperQueryRepository__ctor_ONIONARCH_Application_Abstractions_ConnectionFactory_IDbReadOnlyConnectionFactory_"></a> SampleEntityDapperQueryRepository\(IDbReadOnlyConnectionFactory\)

Dapper implementation of [ISampleEntityDapperQueryRepository](ONIONARCH.Application.Abstractions.Repositories.ISampleEntityDapperQueryRepository.md), executing
parameterized SQL against the <code>SampleTable</code> table in the query database.

```csharp
public SampleEntityDapperQueryRepository(IDbReadOnlyConnectionFactory connectionFactory)
```

#### Parameters

`connectionFactory` IDbReadOnlyConnectionFactory

Creates connections to the query database.

## Methods

### <a id="ONIONARCH_Persistence_Repositories_SampleEntityDapperQueryRepository_GetAllAsync_System_Threading_CancellationToken_"></a> GetAllAsync\(CancellationToken\)

Retrieves every sample entity from the query database.

```csharp
public Task<List<SampleEntityDefinition>> GetAllAsync(CancellationToken cancellationToken = default)
```

#### Parameters

`cancellationToken` [CancellationToken](https://learn.microsoft.com/dotnet/api/system.threading.cancellationtoken)

A token to cancel the operation.

#### Returns

 [Task](https://learn.microsoft.com/dotnet/api/system.threading.tasks.task\-1)<[List](https://learn.microsoft.com/dotnet/api/system.collections.generic.list\-1)<SampleEntityDefinition\>\>

All sample entities (empty if none exist).

### <a id="ONIONARCH_Persistence_Repositories_SampleEntityDapperQueryRepository_GetByIdAsync_System_Int32_System_Threading_CancellationToken_"></a> GetByIdAsync\(int, CancellationToken\)

Retrieves a single sample entity by key.

```csharp
public Task<SampleEntityDefinition?> GetByIdAsync(int sampleId, CancellationToken cancellationToken = default)
```

#### Parameters

`sampleId` [int](https://learn.microsoft.com/dotnet/api/system.int32)

The key of the entity to retrieve.

`cancellationToken` [CancellationToken](https://learn.microsoft.com/dotnet/api/system.threading.cancellationtoken)

A token to cancel the operation.

#### Returns

 [Task](https://learn.microsoft.com/dotnet/api/system.threading.tasks.task\-1)<SampleEntityDefinition?\>

The matching entity, or <a href="https://learn.microsoft.com/dotnet/csharp/language-reference/keywords/null">null</a> if none was found.

