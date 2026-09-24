# <a id="ONIONARCH_Application_Abstractions_Repositories_ISampleEntityDapperCommandRepository"></a> Interface ISampleEntityDapperCommandRepository

Namespace: [ONIONARCH.Application.Abstractions.Repositories](ONIONARCH.Application.Abstractions.Repositories.md)  
Assembly: ONIONARCH.Application.dll  

Write-side port for the Dapper persistence path. Defined in Application, implemented in
Persistence — mirrors [ICommandDbContext](ONIONARCH.Application.Abstractions.Context.ICommandDbContext.md) for the EF Core path so that
Application never depends on Dapper, raw SQL, or [IDbConnection](https://learn.microsoft.com/dotnet/api/system.data.idbconnection).

```csharp
public interface ISampleEntityDapperCommandRepository
```

## Methods

### <a id="ONIONARCH_Application_Abstractions_Repositories_ISampleEntityDapperCommandRepository_CreateAsync_ONIONARCH_Domain_Entities_SampleEntityDefinition_System_Threading_CancellationToken_"></a> CreateAsync\(SampleEntityDefinition, CancellationToken\)

Inserts <code class="paramref">entity</code> into the command database.

```csharp
Task<int> CreateAsync(SampleEntityDefinition entity, CancellationToken cancellationToken = default)
```

#### Parameters

`entity` SampleEntityDefinition

The entity to insert, including its [SampleEntityDefinition.SampleId](ONIONARCH.Domain.Entities.SampleEntityDefinition.md#ONIONARCH_Domain_Entities_SampleEntityDefinition_SampleId).

`cancellationToken` [CancellationToken](https://learn.microsoft.com/dotnet/api/system.threading.cancellationtoken)

A token to cancel the operation.

#### Returns

 [Task](https://learn.microsoft.com/dotnet/api/system.threading.tasks.task\-1)<[int](https://learn.microsoft.com/dotnet/api/system.int32)\>

The number of rows affected.

### <a id="ONIONARCH_Application_Abstractions_Repositories_ISampleEntityDapperCommandRepository_DeleteAsync_System_Int32_System_Threading_CancellationToken_"></a> DeleteAsync\(int, CancellationToken\)

Deletes the row with the given key.

```csharp
Task<int> DeleteAsync(int sampleId, CancellationToken cancellationToken = default)
```

#### Parameters

`sampleId` [int](https://learn.microsoft.com/dotnet/api/system.int32)

The key of the row to delete.

`cancellationToken` [CancellationToken](https://learn.microsoft.com/dotnet/api/system.threading.cancellationtoken)

A token to cancel the operation.

#### Returns

 [Task](https://learn.microsoft.com/dotnet/api/system.threading.tasks.task\-1)<[int](https://learn.microsoft.com/dotnet/api/system.int32)\>

The number of rows affected (0 if no row matched).

### <a id="ONIONARCH_Application_Abstractions_Repositories_ISampleEntityDapperCommandRepository_UpdateAsync_ONIONARCH_Domain_Entities_SampleEntityDefinition_System_Threading_CancellationToken_"></a> UpdateAsync\(SampleEntityDefinition, CancellationToken\)

Updates the row whose key matches <code class="paramref">entity</code>'s
[SampleEntityDefinition.SampleId](ONIONARCH.Domain.Entities.SampleEntityDefinition.md#ONIONARCH_Domain_Entities_SampleEntityDefinition_SampleId) with the entity's current values.

```csharp
Task<int> UpdateAsync(SampleEntityDefinition entity, CancellationToken cancellationToken = default)
```

#### Parameters

`entity` SampleEntityDefinition

The entity carrying the key and new values.

`cancellationToken` [CancellationToken](https://learn.microsoft.com/dotnet/api/system.threading.cancellationtoken)

A token to cancel the operation.

#### Returns

 [Task](https://learn.microsoft.com/dotnet/api/system.threading.tasks.task\-1)<[int](https://learn.microsoft.com/dotnet/api/system.int32)\>

The number of rows affected (0 if no row matched).

