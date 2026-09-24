# <a id="ONIONARCH_Persistence_Repositories_SampleEntityDapperCommandRepository"></a> Class SampleEntityDapperCommandRepository

Namespace: [ONIONARCH.Persistence.Repositories](ONIONARCH.Persistence.Repositories.md)  
Assembly: ONIONARCH.Persistence.dll  

Dapper implementation of [ISampleEntityDapperCommandRepository](ONIONARCH.Application.Abstractions.Repositories.ISampleEntityDapperCommandRepository.md), executing
parameterized SQL against the <code>SampleTable</code> table in the command database.

```csharp
public sealed class SampleEntityDapperCommandRepository : ISampleEntityDapperCommandRepository
```

#### Inheritance

[object](https://learn.microsoft.com/dotnet/api/system.object) ← 
[SampleEntityDapperCommandRepository](ONIONARCH.Persistence.Repositories.SampleEntityDapperCommandRepository.md)

#### Implements

ISampleEntityDapperCommandRepository

#### Inherited Members

[object.Equals\(object?\)](https://learn.microsoft.com/dotnet/api/system.object.equals\#system\-object\-equals\(system\-object\)), 
[object.Equals\(object?, object?\)](https://learn.microsoft.com/dotnet/api/system.object.equals\#system\-object\-equals\(system\-object\-system\-object\)), 
[object.GetHashCode\(\)](https://learn.microsoft.com/dotnet/api/system.object.gethashcode), 
[object.GetType\(\)](https://learn.microsoft.com/dotnet/api/system.object.gettype), 
[object.ReferenceEquals\(object?, object?\)](https://learn.microsoft.com/dotnet/api/system.object.referenceequals), 
[object.ToString\(\)](https://learn.microsoft.com/dotnet/api/system.object.tostring)

## Constructors

### <a id="ONIONARCH_Persistence_Repositories_SampleEntityDapperCommandRepository__ctor_ONIONARCH_Application_Abstractions_ConnectionFactory_IDbWriteConnectionFactory_"></a> SampleEntityDapperCommandRepository\(IDbWriteConnectionFactory\)

Dapper implementation of [ISampleEntityDapperCommandRepository](ONIONARCH.Application.Abstractions.Repositories.ISampleEntityDapperCommandRepository.md), executing
parameterized SQL against the <code>SampleTable</code> table in the command database.

```csharp
public SampleEntityDapperCommandRepository(IDbWriteConnectionFactory connectionFactory)
```

#### Parameters

`connectionFactory` IDbWriteConnectionFactory

Creates connections to the command database.

## Methods

### <a id="ONIONARCH_Persistence_Repositories_SampleEntityDapperCommandRepository_CreateAsync_ONIONARCH_Domain_Entities_SampleEntityDefinition_System_Threading_CancellationToken_"></a> CreateAsync\(SampleEntityDefinition, CancellationToken\)

Inserts <code class="paramref">entity</code> into the command database.

```csharp
public Task<int> CreateAsync(SampleEntityDefinition entity, CancellationToken cancellationToken = default)
```

#### Parameters

`entity` SampleEntityDefinition

The entity to insert, including its [SampleEntityDefinition.SampleId](ONIONARCH.Domain.Entities.SampleEntityDefinition.md#ONIONARCH_Domain_Entities_SampleEntityDefinition_SampleId).

`cancellationToken` [CancellationToken](https://learn.microsoft.com/dotnet/api/system.threading.cancellationtoken)

A token to cancel the operation.

#### Returns

 [Task](https://learn.microsoft.com/dotnet/api/system.threading.tasks.task\-1)<[int](https://learn.microsoft.com/dotnet/api/system.int32)\>

The number of rows affected.

### <a id="ONIONARCH_Persistence_Repositories_SampleEntityDapperCommandRepository_DeleteAsync_System_Int32_System_Threading_CancellationToken_"></a> DeleteAsync\(int, CancellationToken\)

Deletes the row with the given key.

```csharp
public Task<int> DeleteAsync(int sampleId, CancellationToken cancellationToken = default)
```

#### Parameters

`sampleId` [int](https://learn.microsoft.com/dotnet/api/system.int32)

The key of the row to delete.

`cancellationToken` [CancellationToken](https://learn.microsoft.com/dotnet/api/system.threading.cancellationtoken)

A token to cancel the operation.

#### Returns

 [Task](https://learn.microsoft.com/dotnet/api/system.threading.tasks.task\-1)<[int](https://learn.microsoft.com/dotnet/api/system.int32)\>

The number of rows affected (0 if no row matched).

### <a id="ONIONARCH_Persistence_Repositories_SampleEntityDapperCommandRepository_UpdateAsync_ONIONARCH_Domain_Entities_SampleEntityDefinition_System_Threading_CancellationToken_"></a> UpdateAsync\(SampleEntityDefinition, CancellationToken\)

Updates the row whose key matches <code class="paramref">entity</code>'s
[SampleEntityDefinition.SampleId](ONIONARCH.Domain.Entities.SampleEntityDefinition.md#ONIONARCH_Domain_Entities_SampleEntityDefinition_SampleId) with the entity's current values.

```csharp
public Task<int> UpdateAsync(SampleEntityDefinition entity, CancellationToken cancellationToken = default)
```

#### Parameters

`entity` SampleEntityDefinition

The entity carrying the key and new values.

`cancellationToken` [CancellationToken](https://learn.microsoft.com/dotnet/api/system.threading.cancellationtoken)

A token to cancel the operation.

#### Returns

 [Task](https://learn.microsoft.com/dotnet/api/system.threading.tasks.task\-1)<[int](https://learn.microsoft.com/dotnet/api/system.int32)\>

The number of rows affected (0 if no row matched).

