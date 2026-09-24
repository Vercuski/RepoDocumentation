# <a id="ONIONARCH_Persistence_Contexts_CommandDbContext"></a> Class CommandDbContext

Namespace: [ONIONARCH.Persistence.Contexts](ONIONARCH.Persistence.Contexts.md)  
Assembly: ONIONARCH.Persistence.dll  

EF Core context for the write side. Implements both [ICommandDbContext](ONIONARCH.Application.Abstractions.Context.ICommandDbContext.md) and
[IUnitOfWork](ONIONARCH.Application.Abstractions.IUnitOfWork.md), and both are resolved to the same scoped instance so they share
change tracking within a request.

```csharp
public sealed class CommandDbContext : BaseDbContext<CommandDbContext>, IInfrastructure<IServiceProvider>, IDbContextDependencies, IDbSetCache, IDbContextPoolable, IResettableService, IDisposable, IAsyncDisposable, ICommandDbContext, IUnitOfWork
```

#### Inheritance

[object](https://learn.microsoft.com/dotnet/api/system.object) ← 
[DbContext](https://learn.microsoft.com/dotnet/api/microsoft.entityframeworkcore.dbcontext) ← 
[BaseDbContext<CommandDbContext\>](ONIONARCH.Persistence.Contexts.BaseDbContext\-1.md) ← 
[CommandDbContext](ONIONARCH.Persistence.Contexts.CommandDbContext.md)

#### Implements

[IInfrastructure<IServiceProvider\>](https://learn.microsoft.com/dotnet/api/microsoft.entityframeworkcore.infrastructure.iinfrastructure\-1), 
[IDbContextDependencies](https://learn.microsoft.com/dotnet/api/microsoft.entityframeworkcore.internal.idbcontextdependencies), 
[IDbSetCache](https://learn.microsoft.com/dotnet/api/microsoft.entityframeworkcore.internal.idbsetcache), 
[IDbContextPoolable](https://learn.microsoft.com/dotnet/api/microsoft.entityframeworkcore.internal.idbcontextpoolable), 
[IResettableService](https://learn.microsoft.com/dotnet/api/microsoft.entityframeworkcore.infrastructure.iresettableservice), 
[IDisposable](https://learn.microsoft.com/dotnet/api/system.idisposable), 
[IAsyncDisposable](https://learn.microsoft.com/dotnet/api/system.iasyncdisposable), 
ICommandDbContext, 
IUnitOfWork

#### Inherited Members

[BaseDbContext<CommandDbContext\>.SampleEntity](ONIONARCH.Persistence.Contexts.BaseDbContext\-1.md\#ONIONARCH\_Persistence\_Contexts\_BaseDbContext\_1\_SampleEntity), 
[DbContext.Set<TEntity\>\(\)](https://learn.microsoft.com/dotnet/api/microsoft.entityframeworkcore.dbcontext.set\#microsoft\-entityframeworkcore\-dbcontext\-set\-1), 
[DbContext.Set<TEntity\>\(string\)](https://learn.microsoft.com/dotnet/api/microsoft.entityframeworkcore.dbcontext.set\#microsoft\-entityframeworkcore\-dbcontext\-set\-1\(system\-string\)), 
[DbContext.SaveChanges\(\)](https://learn.microsoft.com/dotnet/api/microsoft.entityframeworkcore.dbcontext.savechanges\#microsoft\-entityframeworkcore\-dbcontext\-savechanges), 
[DbContext.SaveChanges\(bool\)](https://learn.microsoft.com/dotnet/api/microsoft.entityframeworkcore.dbcontext.savechanges\#microsoft\-entityframeworkcore\-dbcontext\-savechanges\(system\-boolean\)), 
[DbContext.SaveChangesAsync\(CancellationToken\)](https://learn.microsoft.com/dotnet/api/microsoft.entityframeworkcore.dbcontext.savechangesasync\#microsoft\-entityframeworkcore\-dbcontext\-savechangesasync\(system\-threading\-cancellationtoken\)), 
[DbContext.SaveChangesAsync\(bool, CancellationToken\)](https://learn.microsoft.com/dotnet/api/microsoft.entityframeworkcore.dbcontext.savechangesasync\#microsoft\-entityframeworkcore\-dbcontext\-savechangesasync\(system\-boolean\-system\-threading\-cancellationtoken\)), 
[DbContext.Dispose\(\)](https://learn.microsoft.com/dotnet/api/microsoft.entityframeworkcore.dbcontext.dispose), 
[DbContext.DisposeAsync\(\)](https://learn.microsoft.com/dotnet/api/microsoft.entityframeworkcore.dbcontext.disposeasync), 
[DbContext.Entry<TEntity\>\(TEntity\)](https://learn.microsoft.com/dotnet/api/microsoft.entityframeworkcore.dbcontext.entry\#microsoft\-entityframeworkcore\-dbcontext\-entry\-1\(\-0\)), 
[DbContext.Entry\(object\)](https://learn.microsoft.com/dotnet/api/microsoft.entityframeworkcore.dbcontext.entry\#microsoft\-entityframeworkcore\-dbcontext\-entry\(system\-object\)), 
[DbContext.Add<TEntity\>\(TEntity\)](https://learn.microsoft.com/dotnet/api/microsoft.entityframeworkcore.dbcontext.add\#microsoft\-entityframeworkcore\-dbcontext\-add\-1\(\-0\)), 
[DbContext.AddAsync<TEntity\>\(TEntity, CancellationToken\)](https://learn.microsoft.com/dotnet/api/microsoft.entityframeworkcore.dbcontext.addasync\#microsoft\-entityframeworkcore\-dbcontext\-addasync\-1\(\-0\-system\-threading\-cancellationtoken\)), 
[DbContext.Attach<TEntity\>\(TEntity\)](https://learn.microsoft.com/dotnet/api/microsoft.entityframeworkcore.dbcontext.attach\#microsoft\-entityframeworkcore\-dbcontext\-attach\-1\(\-0\)), 
[DbContext.Update<TEntity\>\(TEntity\)](https://learn.microsoft.com/dotnet/api/microsoft.entityframeworkcore.dbcontext.update\#microsoft\-entityframeworkcore\-dbcontext\-update\-1\(\-0\)), 
[DbContext.Remove<TEntity\>\(TEntity\)](https://learn.microsoft.com/dotnet/api/microsoft.entityframeworkcore.dbcontext.remove\#microsoft\-entityframeworkcore\-dbcontext\-remove\-1\(\-0\)), 
[DbContext.Add\(object\)](https://learn.microsoft.com/dotnet/api/microsoft.entityframeworkcore.dbcontext.add\#microsoft\-entityframeworkcore\-dbcontext\-add\(system\-object\)), 
[DbContext.AddAsync\(object, CancellationToken\)](https://learn.microsoft.com/dotnet/api/microsoft.entityframeworkcore.dbcontext.addasync\#microsoft\-entityframeworkcore\-dbcontext\-addasync\(system\-object\-system\-threading\-cancellationtoken\)), 
[DbContext.Attach\(object\)](https://learn.microsoft.com/dotnet/api/microsoft.entityframeworkcore.dbcontext.attach\#microsoft\-entityframeworkcore\-dbcontext\-attach\(system\-object\)), 
[DbContext.Update\(object\)](https://learn.microsoft.com/dotnet/api/microsoft.entityframeworkcore.dbcontext.update\#microsoft\-entityframeworkcore\-dbcontext\-update\(system\-object\)), 
[DbContext.Remove\(object\)](https://learn.microsoft.com/dotnet/api/microsoft.entityframeworkcore.dbcontext.remove\#microsoft\-entityframeworkcore\-dbcontext\-remove\(system\-object\)), 
[DbContext.AddRange\(params object\[\]\)](https://learn.microsoft.com/dotnet/api/microsoft.entityframeworkcore.dbcontext.addrange\#microsoft\-entityframeworkcore\-dbcontext\-addrange\(system\-object\(\)\)), 
[DbContext.AddRangeAsync\(params object\[\]\)](https://learn.microsoft.com/dotnet/api/microsoft.entityframeworkcore.dbcontext.addrangeasync\#microsoft\-entityframeworkcore\-dbcontext\-addrangeasync\(system\-object\(\)\)), 
[DbContext.AttachRange\(params object\[\]\)](https://learn.microsoft.com/dotnet/api/microsoft.entityframeworkcore.dbcontext.attachrange\#microsoft\-entityframeworkcore\-dbcontext\-attachrange\(system\-object\(\)\)), 
[DbContext.UpdateRange\(params object\[\]\)](https://learn.microsoft.com/dotnet/api/microsoft.entityframeworkcore.dbcontext.updaterange\#microsoft\-entityframeworkcore\-dbcontext\-updaterange\(system\-object\(\)\)), 
[DbContext.RemoveRange\(params object\[\]\)](https://learn.microsoft.com/dotnet/api/microsoft.entityframeworkcore.dbcontext.removerange\#microsoft\-entityframeworkcore\-dbcontext\-removerange\(system\-object\(\)\)), 
[DbContext.AddRange\(IEnumerable<object\>\)](https://learn.microsoft.com/dotnet/api/microsoft.entityframeworkcore.dbcontext.addrange\#microsoft\-entityframeworkcore\-dbcontext\-addrange\(system\-collections\-generic\-ienumerable\(\(system\-object\)\)\)), 
[DbContext.AddRangeAsync\(IEnumerable<object\>, CancellationToken\)](https://learn.microsoft.com/dotnet/api/microsoft.entityframeworkcore.dbcontext.addrangeasync\#microsoft\-entityframeworkcore\-dbcontext\-addrangeasync\(system\-collections\-generic\-ienumerable\(\(system\-object\)\)\-system\-threading\-cancellationtoken\)), 
[DbContext.AttachRange\(IEnumerable<object\>\)](https://learn.microsoft.com/dotnet/api/microsoft.entityframeworkcore.dbcontext.attachrange\#microsoft\-entityframeworkcore\-dbcontext\-attachrange\(system\-collections\-generic\-ienumerable\(\(system\-object\)\)\)), 
[DbContext.UpdateRange\(IEnumerable<object\>\)](https://learn.microsoft.com/dotnet/api/microsoft.entityframeworkcore.dbcontext.updaterange\#microsoft\-entityframeworkcore\-dbcontext\-updaterange\(system\-collections\-generic\-ienumerable\(\(system\-object\)\)\)), 
[DbContext.RemoveRange\(IEnumerable<object\>\)](https://learn.microsoft.com/dotnet/api/microsoft.entityframeworkcore.dbcontext.removerange\#microsoft\-entityframeworkcore\-dbcontext\-removerange\(system\-collections\-generic\-ienumerable\(\(system\-object\)\)\)), 
[DbContext.Find\(Type, params object?\[\]?\)](https://learn.microsoft.com/dotnet/api/microsoft.entityframeworkcore.dbcontext.find\#microsoft\-entityframeworkcore\-dbcontext\-find\(system\-type\-system\-object\(\)\)), 
[DbContext.FindAsync\(Type, params object?\[\]?\)](https://learn.microsoft.com/dotnet/api/microsoft.entityframeworkcore.dbcontext.findasync\#microsoft\-entityframeworkcore\-dbcontext\-findasync\(system\-type\-system\-object\(\)\)), 
[DbContext.FindAsync\(Type, object?\[\]?, CancellationToken\)](https://learn.microsoft.com/dotnet/api/microsoft.entityframeworkcore.dbcontext.findasync\#microsoft\-entityframeworkcore\-dbcontext\-findasync\(system\-type\-system\-object\(\)\-system\-threading\-cancellationtoken\)), 
[DbContext.Find<TEntity\>\(params object?\[\]?\)](https://learn.microsoft.com/dotnet/api/microsoft.entityframeworkcore.dbcontext.find\#microsoft\-entityframeworkcore\-dbcontext\-find\-1\(system\-object\(\)\)), 
[DbContext.FindAsync<TEntity\>\(params object?\[\]?\)](https://learn.microsoft.com/dotnet/api/microsoft.entityframeworkcore.dbcontext.findasync\#microsoft\-entityframeworkcore\-dbcontext\-findasync\-1\(system\-object\(\)\)), 
[DbContext.FindAsync<TEntity\>\(object?\[\]?, CancellationToken\)](https://learn.microsoft.com/dotnet/api/microsoft.entityframeworkcore.dbcontext.findasync\#microsoft\-entityframeworkcore\-dbcontext\-findasync\-1\(system\-object\(\)\-system\-threading\-cancellationtoken\)), 
[DbContext.FromExpression<TResult\>\(Expression<Func<IQueryable<TResult\>\>\>\)](https://learn.microsoft.com/dotnet/api/microsoft.entityframeworkcore.dbcontext.fromexpression), 
[DbContext.Database](https://learn.microsoft.com/dotnet/api/microsoft.entityframeworkcore.dbcontext.database), 
[DbContext.ChangeTracker](https://learn.microsoft.com/dotnet/api/microsoft.entityframeworkcore.dbcontext.changetracker), 
[DbContext.Model](https://learn.microsoft.com/dotnet/api/microsoft.entityframeworkcore.dbcontext.model), 
[DbContext.ContextId](https://learn.microsoft.com/dotnet/api/microsoft.entityframeworkcore.dbcontext.contextid), 
[DbContext.SavingChanges](https://learn.microsoft.com/dotnet/api/microsoft.entityframeworkcore.dbcontext.savingchanges), 
[DbContext.SavedChanges](https://learn.microsoft.com/dotnet/api/microsoft.entityframeworkcore.dbcontext.savedchanges), 
[DbContext.SaveChangesFailed](https://learn.microsoft.com/dotnet/api/microsoft.entityframeworkcore.dbcontext.savechangesfailed), 
[object.Equals\(object?\)](https://learn.microsoft.com/dotnet/api/system.object.equals\#system\-object\-equals\(system\-object\)), 
[object.Equals\(object?, object?\)](https://learn.microsoft.com/dotnet/api/system.object.equals\#system\-object\-equals\(system\-object\-system\-object\)), 
[object.GetHashCode\(\)](https://learn.microsoft.com/dotnet/api/system.object.gethashcode), 
[object.GetType\(\)](https://learn.microsoft.com/dotnet/api/system.object.gettype), 
[object.ReferenceEquals\(object?, object?\)](https://learn.microsoft.com/dotnet/api/system.object.referenceequals), 
[object.ToString\(\)](https://learn.microsoft.com/dotnet/api/system.object.tostring)

## Constructors

### <a id="ONIONARCH_Persistence_Contexts_CommandDbContext__ctor_Microsoft_EntityFrameworkCore_DbContextOptions_ONIONARCH_Persistence_Contexts_CommandDbContext__"></a> CommandDbContext\(DbContextOptions<CommandDbContext\>\)

EF Core context for the write side. Implements both [ICommandDbContext](ONIONARCH.Application.Abstractions.Context.ICommandDbContext.md) and
[IUnitOfWork](ONIONARCH.Application.Abstractions.IUnitOfWork.md), and both are resolved to the same scoped instance so they share
change tracking within a request.

```csharp
public CommandDbContext(DbContextOptions<CommandDbContext> options)
```

#### Parameters

`options` [DbContextOptions](https://learn.microsoft.com/dotnet/api/microsoft.entityframeworkcore.dbcontextoptions\-1)<[CommandDbContext](ONIONARCH.Persistence.Contexts.CommandDbContext.md)\>

The options configured for the command database.

## Methods

### <a id="ONIONARCH_Persistence_Contexts_CommandDbContext_Alter__1___0_"></a> Alter<TEntity\>\(TEntity\)

Stages <code class="paramref">entity</code> for update on the next save. All of its properties are
marked as modified.

```csharp
public void Alter<TEntity>(TEntity entity) where TEntity : Entity
```

#### Parameters

`entity` TEntity

The entity whose current values should be persisted.

#### Type Parameters

`TEntity` 

The domain entity type.

### <a id="ONIONARCH_Persistence_Contexts_CommandDbContext_BeginTransactionAsync_System_Threading_CancellationToken_"></a> BeginTransactionAsync\(CancellationToken\)

Begins a new database transaction on the command database.

```csharp
public Task<IUnitOfWorkTransaction> BeginTransactionAsync(CancellationToken cancellationToken = default)
```

#### Parameters

`cancellationToken` [CancellationToken](https://learn.microsoft.com/dotnet/api/system.threading.cancellationtoken)

A token to cancel the operation.

#### Returns

 [Task](https://learn.microsoft.com/dotnet/api/system.threading.tasks.task\-1)<IUnitOfWorkTransaction\>

A transaction that must be committed or rolled back explicitly and then disposed.

### <a id="ONIONARCH_Persistence_Contexts_CommandDbContext_Delete__1___0_"></a> Delete<TEntity\>\(TEntity\)

Stages <code class="paramref">entity</code> for deletion on the next save.

```csharp
public void Delete<TEntity>(TEntity entity) where TEntity : Entity
```

#### Parameters

`entity` TEntity

The entity to delete.

#### Type Parameters

`TEntity` 

The domain entity type.

### <a id="ONIONARCH_Persistence_Contexts_CommandDbContext_ExecuteSqlAsync_System_String_System_Collections_Generic_IEnumerable_System_Data_IDataParameter__System_Threading_CancellationToken_"></a> ExecuteSqlAsync\(string, IEnumerable<IDataParameter\>, CancellationToken\)

Executes a raw, parameterized SQL statement against the command database immediately,
bypassing change tracking.

```csharp
public Task<int> ExecuteSqlAsync(string sql, IEnumerable<IDataParameter> parameters, CancellationToken cancellationToken = default)
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

### <a id="ONIONARCH_Persistence_Contexts_CommandDbContext_Insert__1___0_"></a> Insert<TEntity\>\(TEntity\)

Stages <code class="paramref">entity</code> for insertion on the next save.

```csharp
public void Insert<TEntity>(TEntity entity) where TEntity : Entity
```

#### Parameters

`entity` TEntity

The entity to insert.

#### Type Parameters

`TEntity` 

The domain entity type.

### <a id="ONIONARCH_Persistence_Contexts_CommandDbContext_InsertRange__1_System_Collections_Generic_IReadOnlyCollection___0__"></a> InsertRange<TEntity\>\(IReadOnlyCollection<TEntity\>\)

Stages every entity in <code class="paramref">entities</code> for insertion on the next save.

```csharp
public void InsertRange<TEntity>(IReadOnlyCollection<TEntity> entities) where TEntity : Entity
```

#### Parameters

`entities` [IReadOnlyCollection](https://learn.microsoft.com/dotnet/api/system.collections.generic.ireadonlycollection\-1)<TEntity\>

The entities to insert.

#### Type Parameters

`TEntity` 

The domain entity type.

### <a id="ONIONARCH_Persistence_Contexts_CommandDbContext_OnModelCreating_Microsoft_EntityFrameworkCore_ModelBuilder_"></a> OnModelCreating\(ModelBuilder\)

Applies every <code>IEntityTypeConfiguration&lt;T&gt;</code> defined in the Persistence assembly
before completing EF Core's default model configuration.

```csharp
protected override void OnModelCreating(ModelBuilder modelBuilder)
```

#### Parameters

`modelBuilder` [ModelBuilder](https://learn.microsoft.com/dotnet/api/microsoft.entityframeworkcore.modelbuilder)

The builder used to construct the model.

### <a id="ONIONARCH_Persistence_Contexts_CommandDbContext_SaveChangesAsync_System_Threading_CancellationToken_"></a> SaveChangesAsync\(CancellationToken\)

Asynchronously persists all staged changes to the command database.

```csharp
public override Task<int> SaveChangesAsync(CancellationToken cancellationToken = default)
```

#### Parameters

`cancellationToken` [CancellationToken](https://learn.microsoft.com/dotnet/api/system.threading.cancellationtoken)

A token to cancel the operation.

#### Returns

 [Task](https://learn.microsoft.com/dotnet/api/system.threading.tasks.task\-1)<[int](https://learn.microsoft.com/dotnet/api/system.int32)\>

The number of state entries written to the database.

