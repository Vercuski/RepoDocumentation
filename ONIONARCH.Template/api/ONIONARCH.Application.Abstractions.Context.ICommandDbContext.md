# <a id="ONIONARCH_Application_Abstractions_Context_ICommandDbContext"></a> Interface ICommandDbContext

Namespace: [ONIONARCH.Application.Abstractions.Context](ONIONARCH.Application.Abstractions.Context.md)  
Assembly: ONIONARCH.Application.dll  

Write-side port for the EF Core persistence path. Defined in Application and implemented by
Persistence's <code>CommandDbContext</code>, so command handlers can stage and save changes
without taking a dependency on EF Core types.

```csharp
public interface ICommandDbContext
```

## Remarks

The staging methods ([ICommandDbContext.Insert<TEntity\>](ONIONARCH.Application.Abstractions.Context.ICommandDbContext.md#ONIONARCH_Application_Abstractions_Context_ICommandDbContext_Insert__1___0_), [ICommandDbContext.Alter<TEntity\>](ONIONARCH.Application.Abstractions.Context.ICommandDbContext.md#ONIONARCH_Application_Abstractions_Context_ICommandDbContext_Alter__1___0_), etc.) only
track changes; nothing reaches the database until [ICommandDbContext.SaveChanges](ONIONARCH.Application.Abstractions.Context.ICommandDbContext.md#ONIONARCH_Application_Abstractions_Context_ICommandDbContext_SaveChanges) is called.

## Methods

### <a id="ONIONARCH_Application_Abstractions_Context_ICommandDbContext_Alter__1___0_"></a> Alter<TEntity\>\(TEntity\)

Stages <code class="paramref">entity</code> for update on the next save. All of its properties are
marked as modified.

```csharp
void Alter<TEntity>(TEntity entity) where TEntity : Entity
```

#### Parameters

`entity` TEntity

The entity whose current values should be persisted.

#### Type Parameters

`TEntity` 

The domain entity type.

### <a id="ONIONARCH_Application_Abstractions_Context_ICommandDbContext_Delete__1___0_"></a> Delete<TEntity\>\(TEntity\)

Stages <code class="paramref">entity</code> for deletion on the next save.

```csharp
void Delete<TEntity>(TEntity entity) where TEntity : Entity
```

#### Parameters

`entity` TEntity

The entity to delete.

#### Type Parameters

`TEntity` 

The domain entity type.

### <a id="ONIONARCH_Application_Abstractions_Context_ICommandDbContext_ExecuteSqlAsync_System_String_System_Collections_Generic_IEnumerable_System_Data_IDataParameter__System_Threading_CancellationToken_"></a> ExecuteSqlAsync\(string, IEnumerable<IDataParameter\>, CancellationToken\)

Executes a raw, parameterized SQL statement against the command database immediately,
bypassing change tracking.

```csharp
Task<int> ExecuteSqlAsync(string sql, IEnumerable<IDataParameter> parameters, CancellationToken cancellationToken = default)
```

#### Parameters

`sql` [string](https://learn.microsoft.com/dotnet/api/system.string)

The SQL statement to execute. Use parameter placeholders; never concatenate user input.

`parameters` [IEnumerable](https://learn.microsoft.com/dotnet/api/system.collections.generic.ienumerable\-1)<[IDataParameter](https://learn.microsoft.com/dotnet/api/system.data.idataparameter)\>

The parameter values referenced by <code class="paramref">sql</code>.

`cancellationToken` [CancellationToken](https://learn.microsoft.com/dotnet/api/system.threading.cancellationtoken)

A token to cancel the operation.

#### Returns

 [Task](https://learn.microsoft.com/dotnet/api/system.threading.tasks.task\-1)<[int](https://learn.microsoft.com/dotnet/api/system.int32)\>

The number of rows affected.

### <a id="ONIONARCH_Application_Abstractions_Context_ICommandDbContext_Insert__1___0_"></a> Insert<TEntity\>\(TEntity\)

Stages <code class="paramref">entity</code> for insertion on the next save.

```csharp
void Insert<TEntity>(TEntity entity) where TEntity : Entity
```

#### Parameters

`entity` TEntity

The entity to insert.

#### Type Parameters

`TEntity` 

The domain entity type.

### <a id="ONIONARCH_Application_Abstractions_Context_ICommandDbContext_InsertRange__1_System_Collections_Generic_IReadOnlyCollection___0__"></a> InsertRange<TEntity\>\(IReadOnlyCollection<TEntity\>\)

Stages every entity in <code class="paramref">entities</code> for insertion on the next save.

```csharp
void InsertRange<TEntity>(IReadOnlyCollection<TEntity> entities) where TEntity : Entity
```

#### Parameters

`entities` [IReadOnlyCollection](https://learn.microsoft.com/dotnet/api/system.collections.generic.ireadonlycollection\-1)<TEntity\>

The entities to insert.

#### Type Parameters

`TEntity` 

The domain entity type.

### <a id="ONIONARCH_Application_Abstractions_Context_ICommandDbContext_SaveChanges"></a> SaveChanges\(\)

Synchronously persists all staged changes to the command database.

```csharp
int SaveChanges()
```

#### Returns

 [int](https://learn.microsoft.com/dotnet/api/system.int32)

The number of state entries written to the database.

