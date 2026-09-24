# <a id="ONIONARCH_Application_Abstractions_IUnitOfWork"></a> Interface IUnitOfWork

Namespace: [ONIONARCH.Application.Abstractions](ONIONARCH.Application.Abstractions.md)  
Assembly: ONIONARCH.Application.dll  

Unit-of-work port over the command database. Lets Application code commit staged changes
asynchronously and group multiple operations in an explicit transaction without depending
on EF Core.

```csharp
public interface IUnitOfWork
```

## Remarks

Implemented by Persistence's <code>CommandDbContext</code>, so within a DI scope it shares change
tracking with [ICommandDbContext](ONIONARCH.Application.Abstractions.Context.ICommandDbContext.md).

## Methods

### <a id="ONIONARCH_Application_Abstractions_IUnitOfWork_BeginTransactionAsync_System_Threading_CancellationToken_"></a> BeginTransactionAsync\(CancellationToken\)

Begins a new database transaction on the command database.

```csharp
Task<IUnitOfWorkTransaction> BeginTransactionAsync(CancellationToken cancellationToken = default)
```

#### Parameters

`cancellationToken` [CancellationToken](https://learn.microsoft.com/dotnet/api/system.threading.cancellationtoken)

A token to cancel the operation.

#### Returns

 [Task](https://learn.microsoft.com/dotnet/api/system.threading.tasks.task\-1)<[IUnitOfWorkTransaction](ONIONARCH.Application.Abstractions.IUnitOfWorkTransaction.md)\>

A transaction that must be committed or rolled back explicitly and then disposed.

### <a id="ONIONARCH_Application_Abstractions_IUnitOfWork_SaveChangesAsync_System_Threading_CancellationToken_"></a> SaveChangesAsync\(CancellationToken\)

Asynchronously persists all staged changes to the command database.

```csharp
Task<int> SaveChangesAsync(CancellationToken cancellationToken = default)
```

#### Parameters

`cancellationToken` [CancellationToken](https://learn.microsoft.com/dotnet/api/system.threading.cancellationtoken)

A token to cancel the operation.

#### Returns

 [Task](https://learn.microsoft.com/dotnet/api/system.threading.tasks.task\-1)<[int](https://learn.microsoft.com/dotnet/api/system.int32)\>

The number of state entries written to the database.

