# <a id="ONIONARCH_Application_Abstractions_Repositories_ISampleEntityDapperQueryRepository"></a> Interface ISampleEntityDapperQueryRepository

Namespace: [ONIONARCH.Application.Abstractions.Repositories](ONIONARCH.Application.Abstractions.Repositories.md)  
Assembly: ONIONARCH.Application.dll  

Read-side port for the Dapper persistence path. Defined in Application, implemented in
Persistence — mirrors [IQueryDbContext](ONIONARCH.Application.Abstractions.Context.IQueryDbContext.md) for the EF Core path so that
Application never depends on Dapper, raw SQL, or [IDbConnection](https://learn.microsoft.com/dotnet/api/system.data.idbconnection).

```csharp
public interface ISampleEntityDapperQueryRepository
```

## Methods

### <a id="ONIONARCH_Application_Abstractions_Repositories_ISampleEntityDapperQueryRepository_GetAllAsync_System_Threading_CancellationToken_"></a> GetAllAsync\(CancellationToken\)

Retrieves every sample entity from the query database.

```csharp
Task<List<SampleEntityDefinition>> GetAllAsync(CancellationToken cancellationToken = default)
```

#### Parameters

`cancellationToken` [CancellationToken](https://learn.microsoft.com/dotnet/api/system.threading.cancellationtoken)

A token to cancel the operation.

#### Returns

 [Task](https://learn.microsoft.com/dotnet/api/system.threading.tasks.task\-1)<[List](https://learn.microsoft.com/dotnet/api/system.collections.generic.list\-1)<SampleEntityDefinition\>\>

All sample entities (empty if none exist).

### <a id="ONIONARCH_Application_Abstractions_Repositories_ISampleEntityDapperQueryRepository_GetByIdAsync_System_Int32_System_Threading_CancellationToken_"></a> GetByIdAsync\(int, CancellationToken\)

Retrieves a single sample entity by key.

```csharp
Task<SampleEntityDefinition?> GetByIdAsync(int sampleId, CancellationToken cancellationToken = default)
```

#### Parameters

`sampleId` [int](https://learn.microsoft.com/dotnet/api/system.int32)

The key of the entity to retrieve.

`cancellationToken` [CancellationToken](https://learn.microsoft.com/dotnet/api/system.threading.cancellationtoken)

A token to cancel the operation.

#### Returns

 [Task](https://learn.microsoft.com/dotnet/api/system.threading.tasks.task\-1)<SampleEntityDefinition?\>

The matching entity, or <a href="https://learn.microsoft.com/dotnet/csharp/language-reference/keywords/null">null</a> if none was found.

