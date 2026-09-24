# <a id="ONIONARCH_Application_Abstractions_IUnitOfWorkTransaction"></a> Interface IUnitOfWorkTransaction

Namespace: [ONIONARCH.Application.Abstractions](ONIONARCH.Application.Abstractions.md)  
Assembly: ONIONARCH.Application.dll  

An explicit database transaction started by [IUnitOfWork.BeginTransactionAsync](ONIONARCH.Application.Abstractions.IUnitOfWork.md#ONIONARCH_Application_Abstractions_IUnitOfWork_BeginTransactionAsync_System_Threading_CancellationToken_).

```csharp
public interface IUnitOfWorkTransaction : IAsyncDisposable
```

#### Implements

[IAsyncDisposable](https://learn.microsoft.com/dotnet/api/system.iasyncdisposable)

## Remarks

Dispose the transaction (<code>await using</code>) when finished. Disposing without calling
[IUnitOfWorkTransaction.CommitAsync](ONIONARCH.Application.Abstractions.IUnitOfWorkTransaction.md#ONIONARCH_Application_Abstractions_IUnitOfWorkTransaction_CommitAsync_System_Threading_CancellationToken_) discards the transaction's work.

## Methods

### <a id="ONIONARCH_Application_Abstractions_IUnitOfWorkTransaction_CommitAsync_System_Threading_CancellationToken_"></a> CommitAsync\(CancellationToken\)

Commits all work performed within the transaction.

```csharp
Task CommitAsync(CancellationToken cancellationToken = default)
```

#### Parameters

`cancellationToken` [CancellationToken](https://learn.microsoft.com/dotnet/api/system.threading.cancellationtoken)

A token to cancel the operation.

#### Returns

 [Task](https://learn.microsoft.com/dotnet/api/system.threading.tasks.task)

A task that completes when the commit has finished.

### <a id="ONIONARCH_Application_Abstractions_IUnitOfWorkTransaction_RollbackAsync_System_Threading_CancellationToken_"></a> RollbackAsync\(CancellationToken\)

Rolls back all work performed within the transaction.

```csharp
Task RollbackAsync(CancellationToken cancellationToken = default)
```

#### Parameters

`cancellationToken` [CancellationToken](https://learn.microsoft.com/dotnet/api/system.threading.cancellationtoken)

A token to cancel the operation.

#### Returns

 [Task](https://learn.microsoft.com/dotnet/api/system.threading.tasks.task)

A task that completes when the rollback has finished.

