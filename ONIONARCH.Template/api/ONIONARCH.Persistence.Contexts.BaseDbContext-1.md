# <a id="ONIONARCH_Persistence_Contexts_BaseDbContext_1"></a> Class BaseDbContext<T\>

Namespace: [ONIONARCH.Persistence.Contexts](ONIONARCH.Persistence.Contexts.md)  
Assembly: ONIONARCH.Persistence.dll  

Shared EF Core model for the command and query contexts. Declare entity sets here so both
sides of the CQRS split map the same schema.

```csharp
public abstract class BaseDbContext<T> : DbContext, IInfrastructure<IServiceProvider>, IDbContextDependencies, IDbSetCache, IDbContextPoolable, IResettableService, IDisposable, IAsyncDisposable where T : DbContext
```

#### Type Parameters

`T` 

The concrete derived context type, so each derived context receives its own strongly typed
[DbContextOptions](https://learn.microsoft.com/dotnet/api/microsoft.entityframeworkcore.dbcontextoptions-1) from DI.

#### Inheritance

[object](https://learn.microsoft.com/dotnet/api/system.object) ← 
[DbContext](https://learn.microsoft.com/dotnet/api/microsoft.entityframeworkcore.dbcontext) ← 
[BaseDbContext<T\>](ONIONARCH.Persistence.Contexts.BaseDbContext\-1.md)

#### Implements

[IInfrastructure<IServiceProvider\>](https://learn.microsoft.com/dotnet/api/microsoft.entityframeworkcore.infrastructure.iinfrastructure\-1), 
[IDbContextDependencies](https://learn.microsoft.com/dotnet/api/microsoft.entityframeworkcore.internal.idbcontextdependencies), 
[IDbSetCache](https://learn.microsoft.com/dotnet/api/microsoft.entityframeworkcore.internal.idbsetcache), 
[IDbContextPoolable](https://learn.microsoft.com/dotnet/api/microsoft.entityframeworkcore.internal.idbcontextpoolable), 
[IResettableService](https://learn.microsoft.com/dotnet/api/microsoft.entityframeworkcore.infrastructure.iresettableservice), 
[IDisposable](https://learn.microsoft.com/dotnet/api/system.idisposable), 
[IAsyncDisposable](https://learn.microsoft.com/dotnet/api/system.iasyncdisposable)

#### Inherited Members

[DbContext.Set<TEntity\>\(\)](https://learn.microsoft.com/dotnet/api/microsoft.entityframeworkcore.dbcontext.set\#microsoft\-entityframeworkcore\-dbcontext\-set\-1), 
[DbContext.Set<TEntity\>\(string\)](https://learn.microsoft.com/dotnet/api/microsoft.entityframeworkcore.dbcontext.set\#microsoft\-entityframeworkcore\-dbcontext\-set\-1\(system\-string\)), 
[DbContext.OnConfiguring\(DbContextOptionsBuilder\)](https://learn.microsoft.com/dotnet/api/microsoft.entityframeworkcore.dbcontext.onconfiguring), 
[DbContext.ConfigureConventions\(ModelConfigurationBuilder\)](https://learn.microsoft.com/dotnet/api/microsoft.entityframeworkcore.dbcontext.configureconventions), 
[DbContext.OnModelCreating\(ModelBuilder\)](https://learn.microsoft.com/dotnet/api/microsoft.entityframeworkcore.dbcontext.onmodelcreating), 
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
[object.MemberwiseClone\(\)](https://learn.microsoft.com/dotnet/api/system.object.memberwiseclone), 
[object.ReferenceEquals\(object?, object?\)](https://learn.microsoft.com/dotnet/api/system.object.referenceequals), 
[object.ToString\(\)](https://learn.microsoft.com/dotnet/api/system.object.tostring)

## Constructors

### <a id="ONIONARCH_Persistence_Contexts_BaseDbContext_1__ctor_Microsoft_EntityFrameworkCore_DbContextOptions__0__"></a> BaseDbContext\(DbContextOptions<T\>\)

Shared EF Core model for the command and query contexts. Declare entity sets here so both
sides of the CQRS split map the same schema.

```csharp
protected BaseDbContext(DbContextOptions<T> options)
```

#### Parameters

`options` [DbContextOptions](https://learn.microsoft.com/dotnet/api/microsoft.entityframeworkcore.dbcontextoptions\-1)<T\>

The options for the derived context.

## Properties

### <a id="ONIONARCH_Persistence_Contexts_BaseDbContext_1_SampleEntity"></a> SampleEntity

Gets or sets the set of [SampleEntityDefinition](ONIONARCH.Domain.Entities.SampleEntityDefinition.md) entities.

```csharp
public DbSet<SampleEntityDefinition> SampleEntity { get; set; }
```

#### Property Value

 [DbSet](https://learn.microsoft.com/dotnet/api/microsoft.entityframeworkcore.dbset\-1)<SampleEntityDefinition\>

