# <a id="ONIONARCH_Persistence_Contexts_QueryDbContext"></a> Class QueryDbContext

Namespace: [ONIONARCH.Persistence.Contexts](ONIONARCH.Persistence.Contexts.md)  
Assembly: ONIONARCH.Persistence.dll  

EF Core context for the read side, configured for no-tracking queries.

```csharp
public sealed class QueryDbContext : BaseDbContext<QueryDbContext>, IInfrastructure<IServiceProvider>, IDbContextDependencies, IDbSetCache, IDbContextPoolable, IResettableService, IDisposable, IAsyncDisposable, IQueryDbContext
```

#### Inheritance

[object](https://learn.microsoft.com/dotnet/api/system.object) ← 
[DbContext](https://learn.microsoft.com/dotnet/api/microsoft.entityframeworkcore.dbcontext) ← 
[BaseDbContext<QueryDbContext\>](ONIONARCH.Persistence.Contexts.BaseDbContext\-1.md) ← 
[QueryDbContext](ONIONARCH.Persistence.Contexts.QueryDbContext.md)

#### Implements

[IInfrastructure<IServiceProvider\>](https://learn.microsoft.com/dotnet/api/microsoft.entityframeworkcore.infrastructure.iinfrastructure\-1), 
[IDbContextDependencies](https://learn.microsoft.com/dotnet/api/microsoft.entityframeworkcore.internal.idbcontextdependencies), 
[IDbSetCache](https://learn.microsoft.com/dotnet/api/microsoft.entityframeworkcore.internal.idbsetcache), 
[IDbContextPoolable](https://learn.microsoft.com/dotnet/api/microsoft.entityframeworkcore.internal.idbcontextpoolable), 
[IResettableService](https://learn.microsoft.com/dotnet/api/microsoft.entityframeworkcore.infrastructure.iresettableservice), 
[IDisposable](https://learn.microsoft.com/dotnet/api/system.idisposable), 
[IAsyncDisposable](https://learn.microsoft.com/dotnet/api/system.iasyncdisposable), 
IQueryDbContext

#### Inherited Members

[BaseDbContext<QueryDbContext\>.SampleEntity](ONIONARCH.Persistence.Contexts.BaseDbContext\-1.md\#ONIONARCH\_Persistence\_Contexts\_BaseDbContext\_1\_SampleEntity), 
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

### <a id="ONIONARCH_Persistence_Contexts_QueryDbContext__ctor_Microsoft_EntityFrameworkCore_DbContextOptions_ONIONARCH_Persistence_Contexts_QueryDbContext__"></a> QueryDbContext\(DbContextOptions<QueryDbContext\>\)

EF Core context for the read side, configured for no-tracking queries.

```csharp
public QueryDbContext(DbContextOptions<QueryDbContext> options)
```

#### Parameters

`options` [DbContextOptions](https://learn.microsoft.com/dotnet/api/microsoft.entityframeworkcore.dbcontextoptions\-1)<[QueryDbContext](ONIONARCH.Persistence.Contexts.QueryDbContext.md)\>

The options configured for the query database.

## Methods

### <a id="ONIONARCH_Persistence_Contexts_QueryDbContext_OnConfiguring_Microsoft_EntityFrameworkCore_DbContextOptionsBuilder_"></a> OnConfiguring\(DbContextOptionsBuilder\)

Sets [NoTracking](https://learn.microsoft.com/dotnet/api/microsoft.entityframeworkcore.querytrackingbehavior.notracking) as the default for this context, since
entities read here are never saved back through it.

```csharp
protected override void OnConfiguring(DbContextOptionsBuilder optionsBuilder)
```

#### Parameters

`optionsBuilder` [DbContextOptionsBuilder](https://learn.microsoft.com/dotnet/api/microsoft.entityframeworkcore.dbcontextoptionsbuilder)

The builder used to configure the context.

### <a id="ONIONARCH_Persistence_Contexts_QueryDbContext_OnModelCreating_Microsoft_EntityFrameworkCore_ModelBuilder_"></a> OnModelCreating\(ModelBuilder\)

Applies every <code>IEntityTypeConfiguration&lt;T&gt;</code> defined in the Persistence assembly
before completing EF Core's default model configuration.

```csharp
protected override void OnModelCreating(ModelBuilder modelBuilder)
```

#### Parameters

`modelBuilder` [ModelBuilder](https://learn.microsoft.com/dotnet/api/microsoft.entityframeworkcore.modelbuilder)

The builder used to construct the model.

### <a id="ONIONARCH_Persistence_Contexts_QueryDbContext_SingleOrDefaultAsync__1_System_Linq_IQueryable___0__System_Threading_CancellationToken_"></a> SingleOrDefaultAsync<TEntity\>\(IQueryable<TEntity\>, CancellationToken\)

Asynchronously executes <code class="paramref">query</code> and returns its single result, or
<a href="https://learn.microsoft.com/dotnet/csharp/language-reference/keywords/null">null</a> if it matched nothing.

```csharp
public Task<TEntity?> SingleOrDefaultAsync<TEntity>(IQueryable<TEntity> query, CancellationToken cancellationToken = default) where TEntity : Entity
```

#### Parameters

`query` [IQueryable](https://learn.microsoft.com/dotnet/api/system.linq.iqueryable\-1)<TEntity\>

A query obtained from [IQueryDbContext.Set<TEntity\>](ONIONARCH.Application.Abstractions.Context.IQueryDbContext.md#ONIONARCH_Application_Abstractions_Context_IQueryDbContext_Set__1).

`cancellationToken` [CancellationToken](https://learn.microsoft.com/dotnet/api/system.threading.cancellationtoken)

A token to cancel the operation.

#### Returns

 [Task](https://learn.microsoft.com/dotnet/api/system.threading.tasks.task\-1)<TEntity?\>

The matching entity, or <a href="https://learn.microsoft.com/dotnet/csharp/language-reference/keywords/null">null</a> if none was found.

#### Type Parameters

`TEntity` 

The domain entity type.

#### Exceptions

 [InvalidOperationException](https://learn.microsoft.com/dotnet/api/system.invalidoperationexception)

The query matched more than one entity.

### <a id="ONIONARCH_Persistence_Contexts_QueryDbContext_ToListAsync__1_System_Linq_IQueryable___0__System_Threading_CancellationToken_"></a> ToListAsync<TEntity\>\(IQueryable<TEntity\>, CancellationToken\)

Asynchronously executes <code class="paramref">query</code> and materializes the results into a list.

```csharp
public Task<List<TEntity>> ToListAsync<TEntity>(IQueryable<TEntity> query, CancellationToken cancellationToken = default) where TEntity : Entity
```

#### Parameters

`query` [IQueryable](https://learn.microsoft.com/dotnet/api/system.linq.iqueryable\-1)<TEntity\>

A query obtained from [IQueryDbContext.Set<TEntity\>](ONIONARCH.Application.Abstractions.Context.IQueryDbContext.md#ONIONARCH_Application_Abstractions_Context_IQueryDbContext_Set__1).

`cancellationToken` [CancellationToken](https://learn.microsoft.com/dotnet/api/system.threading.cancellationtoken)

A token to cancel the operation.

#### Returns

 [Task](https://learn.microsoft.com/dotnet/api/system.threading.tasks.task\-1)<[List](https://learn.microsoft.com/dotnet/api/system.collections.generic.list\-1)<TEntity\>\>

A list containing every entity matched by the query (empty if none).

#### Type Parameters

`TEntity` 

The domain entity type.

